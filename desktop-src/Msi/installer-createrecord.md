---
description: Die Methode "kreaterecord" des Installer-Objekts gibt ein neues Datensatz-Objekt mit der angeforderten Anzahl von Feldern zurück.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer. kreaterecord-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365437"
---
# <a name="installercreaterecord-method"></a><span data-ttu-id="62f70-103">Installer. kreaterecord-Methode</span><span class="sxs-lookup"><span data-stu-id="62f70-103">Installer.CreateRecord method</span></span>

<span data-ttu-id="62f70-104">Die Methode " **kreaterecord** " des [**Installer**](installer-object.md) -Objekts gibt ein neues [**Datensatz**](record-object.md) -Objekt mit der angeforderten Anzahl von Feldern zurück.</span><span class="sxs-lookup"><span data-stu-id="62f70-104">The **CreateRecord** method of the [**Installer**](installer-object.md) object returns a new [**Record**](record-object.md) object with the requested number of fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62f70-105">Syntax</span></span>


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a><span data-ttu-id="62f70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62f70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62f70-107">*count*</span><span class="sxs-lookup"><span data-stu-id="62f70-107">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="62f70-108">Erforderliche Anzahl von Feldern, die möglicherweise 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="62f70-108">Required number of fields, which may be 0.</span></span> <span data-ttu-id="62f70-109">Die maximale Anzahl von Feldern in einem Datensatz ist auf 65535 beschränkt.</span><span class="sxs-lookup"><span data-stu-id="62f70-109">The maximum number of fields in a record is limited to 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62f70-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62f70-110">Return value</span></span>

<span data-ttu-id="62f70-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="62f70-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62f70-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62f70-112">Remarks</span></span>

<span data-ttu-id="62f70-113">Feld 0, nicht eines der Felder in *count*, wird normalerweise für Daten Satz orientierte Elemente verwendet, z. b. Format Zeichenfolgen oder Ausführungs-op-Codes.</span><span class="sxs-lookup"><span data-stu-id="62f70-113">Field 0, not one of the fields in *count*, is normally used for record-oriented items such as format strings or execution op-codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f70-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62f70-114">Requirements</span></span>



| <span data-ttu-id="62f70-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62f70-115">Requirement</span></span> | <span data-ttu-id="62f70-116">Wert</span><span class="sxs-lookup"><span data-stu-id="62f70-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f70-117">Version</span><span class="sxs-lookup"><span data-stu-id="62f70-117">Version</span></span><br/> | <span data-ttu-id="62f70-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62f70-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62f70-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62f70-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62f70-120">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="62f70-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="62f70-121">DLL</span><span class="sxs-lookup"><span data-stu-id="62f70-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="62f70-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62f70-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="62f70-123">IID</span><span class="sxs-lookup"><span data-stu-id="62f70-123">IID</span></span><br/>     | <span data-ttu-id="62f70-124">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="62f70-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




