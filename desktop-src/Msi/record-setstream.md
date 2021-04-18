---
description: Mit der setStream-Methode des Datensatz-Objekts wird der Inhalt der angegebenen Datei als Streamdaten in das angegebene Daten Satz Feld kopiert. Streamdaten können nicht in temporäre Felder eingefügt werden.
ms.assetid: feb79371-d0c4-4bb0-b539-2f431ee1051b
title: Record. setStream-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.SetStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 94ec3d63b3dcd75a13c2c0ff62b624b89979d641
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360961"
---
# <a name="recordsetstream-method"></a><span data-ttu-id="65aaf-104">Record. setStream-Methode</span><span class="sxs-lookup"><span data-stu-id="65aaf-104">Record.SetStream method</span></span>

<span data-ttu-id="65aaf-105">Mit der **setStream** -Methode des [**Datensatz**](record-object.md) -Objekts wird der Inhalt der angegebenen Datei als Streamdaten in das angegebene Daten Satz Feld kopiert.</span><span class="sxs-lookup"><span data-stu-id="65aaf-105">The **SetStream** method of the [**Record**](record-object.md) object copies the content of the specified file into the designated record field as stream data.</span></span> <span data-ttu-id="65aaf-106">Streamdaten können nicht in temporäre Felder eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="65aaf-106">Stream data cannot be inserted into temporary fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="65aaf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="65aaf-107">Syntax</span></span>


```JScript
Record.SetStream(
  field,
  filePath
)
```



## <a name="parameters"></a><span data-ttu-id="65aaf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="65aaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65aaf-109">*Flächen*</span><span class="sxs-lookup"><span data-stu-id="65aaf-109">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="65aaf-110">Erforderliche Feldnummer des Werts im Datensatz, 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="65aaf-110">Required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="65aaf-111">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="65aaf-111">*filePath*</span></span> 
</dt> <dd>

<span data-ttu-id="65aaf-112">Der Speicherort der zu kopierenden Datei.</span><span class="sxs-lookup"><span data-stu-id="65aaf-112">The location of the file to copy.</span></span> <span data-ttu-id="65aaf-113">Es wird keine Übersetzung eines beliebigen Typs durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="65aaf-113">No translation of any type is performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65aaf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65aaf-114">Return value</span></span>

<span data-ttu-id="65aaf-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="65aaf-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65aaf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65aaf-116">Remarks</span></span>

<span data-ttu-id="65aaf-117">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="65aaf-117">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="65aaf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65aaf-118">Requirements</span></span>



| <span data-ttu-id="65aaf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65aaf-119">Requirement</span></span> | <span data-ttu-id="65aaf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="65aaf-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65aaf-121">Version</span><span class="sxs-lookup"><span data-stu-id="65aaf-121">Version</span></span><br/> | <span data-ttu-id="65aaf-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65aaf-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="65aaf-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="65aaf-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="65aaf-124">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="65aaf-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="65aaf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="65aaf-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="65aaf-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65aaf-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="65aaf-127">IID</span><span class="sxs-lookup"><span data-stu-id="65aaf-127">IID</span></span><br/>     | <span data-ttu-id="65aaf-128">IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="65aaf-128">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




