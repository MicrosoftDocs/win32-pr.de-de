---
title: GetIcon-Methode der Win32_TSGetIcon-Klasse
description: Gibt den Inhalt des angegebenen Symbols zurück.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- GetIcon-Methode Remotedesktopdienste
- GetIcon-Methode Remotedesktopdienste, Win32_TSGetIcon-Klasse
- Win32_TSGetIcon-Klasse Remotedesktopdienste, GetIcon-Methode
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949505"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="b2c3a-106">GetIcon-Methode der Win32- \_ Klasse "zgeticon"</span><span class="sxs-lookup"><span data-stu-id="b2c3a-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="b2c3a-107">Gibt den Inhalt des angegebenen Symbols zurück.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c3a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c3a-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="b2c3a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c3a-110">*FilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c3a-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c3a-111">Gibt den Pfad zu der Datei an, in der das Symbol enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="b2c3a-112">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2c3a-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c3a-113">Gibt den Index des Symbols in der Datei an.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="b2c3a-114">*Iconcontent* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b2c3a-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c3a-115">Nach erfolgreichem Abschluss enthält der Inhalt des Symbols.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2c3a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2c3a-116">Requirements</span></span>



| <span data-ttu-id="b2c3a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2c3a-117">Requirement</span></span> | <span data-ttu-id="b2c3a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b2c3a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c3a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2c3a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c3a-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b2c3a-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b2c3a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2c3a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c3a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2c3a-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="b2c3a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2c3a-123">Namespace</span></span><br/>                | <span data-ttu-id="b2c3a-124">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b2c3a-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b2c3a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="b2c3a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2c3a-126"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b2c3a-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="b2c3a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b2c3a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2c3a-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2c3a-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c3a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2c3a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c3a-130">**Win32-Zeit \_ Ticon**</span><span class="sxs-lookup"><span data-stu-id="b2c3a-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





