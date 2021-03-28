---
description: Öffnet ein angegebenes Volume und initialisiert dessen Kontingent Steuerungsobjekt.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Initialize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977176"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="ccecb-103">DiskQuotaControl.Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="ccecb-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="ccecb-104">Öffnet ein angegebenes Volume und initialisiert dessen Kontingent Steuerungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ccecb-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccecb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccecb-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="ccecb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccecb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccecb-107">*Spath*</span><span class="sxs-lookup"><span data-stu-id="ccecb-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="ccecb-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ccecb-108">Type: **String**</span></span>

<span data-ttu-id="ccecb-109">Ein Zeichen folgen Wert, der den voll qualifizierten Pfad des zu initialisierenden Volumes enthält.</span><span class="sxs-lookup"><span data-stu-id="ccecb-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="ccecb-110">*breadwrite*</span><span class="sxs-lookup"><span data-stu-id="ccecb-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="ccecb-111">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ccecb-111">Type: **Boolean**</span></span>

<span data-ttu-id="ccecb-112">Ein boolescher Wert, der angibt, wie das Volume geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccecb-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="ccecb-113">Legen Sie *breadwrite* für Lese-/Schreibzugriff auf " **true** " oder " **false** " für schreibgeschützten Zugriff fest.</span><span class="sxs-lookup"><span data-stu-id="ccecb-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccecb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccecb-114">Return value</span></span>

<span data-ttu-id="ccecb-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ccecb-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccecb-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ccecb-116">Requirements</span></span>



| <span data-ttu-id="ccecb-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccecb-117">Requirement</span></span> | <span data-ttu-id="ccecb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ccecb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccecb-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccecb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ccecb-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccecb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccecb-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccecb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ccecb-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccecb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ccecb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ccecb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccecb-124"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ccecb-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccecb-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ccecb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccecb-126">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="ccecb-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




