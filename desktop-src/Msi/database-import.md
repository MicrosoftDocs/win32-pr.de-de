---
description: Mit der Import-Methode des Datenbankobjekts wird eine Datenbanktabelle aus einer Textarchiv Datei importiert, wobei alle vorhandenen Tabellen gelöscht werden.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370070"
---
# <a name="databaseimport-method"></a><span data-ttu-id="9aa80-103">Database. Import-Methode</span><span class="sxs-lookup"><span data-stu-id="9aa80-103">Database.Import method</span></span>

<span data-ttu-id="9aa80-104">Mit der **Import** -Methode des [**Daten Bank**](database-object.md) Objekts wird eine Datenbanktabelle aus einer [Textarchiv Datei](text-archive-files.md)importiert, wobei alle vorhandenen Tabellen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9aa80-104">The **Import** method of the [**Database**](database-object.md) object imports a database table from a [text archive files](text-archive-files.md), dropping any existing table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9aa80-105">Syntax</span></span>


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a><span data-ttu-id="9aa80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9aa80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa80-107">*path*</span><span class="sxs-lookup"><span data-stu-id="9aa80-107">*path*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa80-108">Erforderlicher Ordner, in dem die Textdatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9aa80-108">Required folder where the text file is present.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-109">*datei*</span><span class="sxs-lookup"><span data-stu-id="9aa80-109">*file*</span></span> 
</dt> <dd>

<span data-ttu-id="9aa80-110">Der erforderliche Name der zu importierenden Datei.</span><span class="sxs-lookup"><span data-stu-id="9aa80-110">Required name of the file to be imported.</span></span> <span data-ttu-id="9aa80-111">Dies schließt den Ordner nicht ein, da dieser im Path-Objekt festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="9aa80-111">This does not include the folder, as that must be set in the path object.</span></span> <span data-ttu-id="9aa80-112">Der Tabellenname wird in der Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="9aa80-112">The table name is specified within the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa80-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9aa80-113">Return value</span></span>

<span data-ttu-id="9aa80-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9aa80-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa80-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9aa80-115">Remarks</span></span>

<span data-ttu-id="9aa80-116">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="9aa80-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa80-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9aa80-117">Requirements</span></span>



| <span data-ttu-id="9aa80-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9aa80-118">Requirement</span></span> | <span data-ttu-id="9aa80-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9aa80-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa80-120">Version</span><span class="sxs-lookup"><span data-stu-id="9aa80-120">Version</span></span><br/> | <span data-ttu-id="9aa80-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9aa80-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9aa80-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9aa80-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9aa80-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="9aa80-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9aa80-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9aa80-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="9aa80-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa80-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9aa80-126">IID</span><span class="sxs-lookup"><span data-stu-id="9aa80-126">IID</span></span><br/>     | <span data-ttu-id="9aa80-127">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9aa80-127">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9aa80-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aa80-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa80-129">**Verbindung**</span><span class="sxs-lookup"><span data-stu-id="9aa80-129">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="9aa80-130">**Msidatabaseimport**</span><span class="sxs-lookup"><span data-stu-id="9aa80-130">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




