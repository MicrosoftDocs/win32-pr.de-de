---
description: Entfernt eine Netzwerk-oder URL-Quelle.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Patch. sourcelistclearsource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351229"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="ae8b7-103">Patch. sourcelistclearsource-Methode</span><span class="sxs-lookup"><span data-stu-id="ae8b7-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="ae8b7-104">Die **sourcelistclearsource** -Methode entfernt eine Netzwerk-oder URL-Quelle.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="ae8b7-105">Diese Methode ruft [**msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)auf.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8b7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae8b7-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="ae8b7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae8b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae8b7-108">*Type*</span><span class="sxs-lookup"><span data-stu-id="ae8b7-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8b7-109">Der Typ der Quelle, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="ae8b7-110">**msisourcetype- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="ae8b7-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="ae8b7-111">**msisourcetype- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="ae8b7-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="ae8b7-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="ae8b7-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="ae8b7-113">Der Pfad zur Quelle, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae8b7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae8b7-114">Return value</span></span>

<span data-ttu-id="ae8b7-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae8b7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae8b7-116">Requirements</span></span>



| <span data-ttu-id="ae8b7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae8b7-117">Requirement</span></span> | <span data-ttu-id="ae8b7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ae8b7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8b7-119">Version</span><span class="sxs-lookup"><span data-stu-id="ae8b7-119">Version</span></span><br/> | <span data-ttu-id="ae8b7-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ae8b7-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ae8b7-122">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ae8b7-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ae8b7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ae8b7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ae8b7-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae8b7-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ae8b7-125">IID</span><span class="sxs-lookup"><span data-stu-id="ae8b7-125">IID</span></span><br/>     | <span data-ttu-id="ae8b7-126">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ae8b7-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="ae8b7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae8b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae8b7-128">**Patch**</span><span class="sxs-lookup"><span data-stu-id="ae8b7-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="ae8b7-129">**Msisourcelistclearsource**</span><span class="sxs-lookup"><span data-stu-id="ae8b7-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="ae8b7-130">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae8b7-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




