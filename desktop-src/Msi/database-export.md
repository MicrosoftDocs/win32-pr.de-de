---
description: Die Export-Methode des Datenbankobjekts kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine Textarchiv Datei.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370025"
---
# <a name="databaseexport-method"></a><span data-ttu-id="8b915-103">Database. Export-Methode</span><span class="sxs-lookup"><span data-stu-id="8b915-103">Database.Export method</span></span>

<span data-ttu-id="8b915-104">Die **Export** -Methode des [**Daten Bank**](database-object.md) Objekts kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine [Textarchiv Datei](text-archive-files.md).</span><span class="sxs-lookup"><span data-stu-id="8b915-104">The **Export** method of the [**Database**](database-object.md) object copies the structure and data from a specified table to a [text archive file](text-archive-files.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b915-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b915-105">Syntax</span></span>


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="8b915-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b915-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b915-107">*Tabelle*</span><span class="sxs-lookup"><span data-stu-id="8b915-107">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="8b915-108">Der erforderliche Name der Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="8b915-108">Required name of the database table.</span></span> <span data-ttu-id="8b915-109">Unterscheidung nach Groß-/Kleinschreibung bei Verwendung der Installer-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8b915-109">Case-sensitive if using the installer database.</span></span>

</dd> <dt>

<span data-ttu-id="8b915-110">*path*</span><span class="sxs-lookup"><span data-stu-id="8b915-110">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="8b915-111">Erforderliche Zeichenfolge, die der Pfad zu dem Ordner ist, in dem die Textdatei abgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8b915-111">Required string that is the path to the folder where the text file is placed.</span></span>

</dd> <dt>

<span data-ttu-id="8b915-112">*datei*</span><span class="sxs-lookup"><span data-stu-id="8b915-112">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="8b915-113">Der erforderliche Name der zu erstellenden Datei.</span><span class="sxs-lookup"><span data-stu-id="8b915-113">Required name of the file to be created.</span></span> <span data-ttu-id="8b915-114">Dies schließt den Ordner nicht ein, da dieser im Path-Objekt festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b915-114">This does not include the folder, as that must be set in the path object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b915-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b915-115">Return value</span></span>

<span data-ttu-id="8b915-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8b915-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b915-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b915-117">Remarks</span></span>

<span data-ttu-id="8b915-118">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="8b915-118">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b915-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b915-119">Requirements</span></span>



| <span data-ttu-id="8b915-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b915-120">Requirement</span></span> | <span data-ttu-id="8b915-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8b915-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b915-122">Version</span><span class="sxs-lookup"><span data-stu-id="8b915-122">Version</span></span><br/> | <span data-ttu-id="8b915-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8b915-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8b915-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8b915-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8b915-125">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="8b915-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8b915-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8b915-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="8b915-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b915-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8b915-128">IID</span><span class="sxs-lookup"><span data-stu-id="8b915-128">IID</span></span><br/>     | <span data-ttu-id="8b915-129">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8b915-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




