import List\nimport uuid\nfrom

datetime import

datetime\n\n\nROOT_DIR =

Path(__file__).parent\nload_dotenv

(ROOT_DIR / \'

.env\')\n\n#

MongoDB connection\nmongo_url

=

os.environ[\'MONGO_URL\']\nclient

=

AsyncIOMotorClient(mongo_url)\n

db =

client[os.environ[\'DB_NAME\']]\n\n

# Create the main app without a

prefix\napp = FastAPI()\n\n# Create

a router with the /api

prefix\napi_router =

APIRouter(prefix="/api")\n\n\n#
