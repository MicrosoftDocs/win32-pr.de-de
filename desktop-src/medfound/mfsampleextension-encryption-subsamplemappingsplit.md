---
description: Legt die unter Stichproben Zuordnung für das Beispiel fest, das die unverschlüsselten und verschlüsselten Bytes in den Beispiel Daten angibt.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: MFSampleExtension_Encryption_SubSampleMappingSplit-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356582"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="f5147-103">MF SampleExtension \_ Encryption \_ subsamplemappingsplit-Attribut</span><span class="sxs-lookup"><span data-stu-id="f5147-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="f5147-104">Legt die unter Stichproben Zuordnung für das Beispiel fest, das die unverschlüsselten und verschlüsselten Bytes in den Beispiel Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="f5147-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5147-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f5147-105">Data type</span></span>

<span data-ttu-id="f5147-106">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="f5147-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="f5147-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5147-107">Remarks</span></span>

<span data-ttu-id="f5147-108">Das **BLOB** muss ein Array von Byte Bereichen als DWords enthalten, wobei jede zweier DWords eine Menge macht.</span><span class="sxs-lookup"><span data-stu-id="f5147-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="f5147-109">Das erste DWORD in jeder Gruppe ist die Anzahl der eindeutigen bytes, und das zweite DWORD des Satzes ist die Anzahl verschlüsselter Bytes.</span><span class="sxs-lookup"><span data-stu-id="f5147-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="f5147-110">Beachten Sie, dass es sich bei einem Paar von 0s nicht um einen gültigen Satz handelt (jeder Wert kann 0 sein, aber nicht beides).</span><span class="sxs-lookup"><span data-stu-id="f5147-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="f5147-111">Das Array von Byte Bereichen gibt an, welche Bereiche entschlüsselt werden sollen, einschließlich der Möglichkeit, dass die gesamte Stichprobe nicht entschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5147-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="f5147-112">Es wird empfohlen, dass dies nicht für klare Beispiele festgelegt wird, obwohl es möglich ist, dasselbe Ergebnis zu erzielen, indem es die entsprechenden Werte festlegt.</span><span class="sxs-lookup"><span data-stu-id="f5147-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="f5147-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5147-113">Examples</span></span>

<span data-ttu-id="f5147-114">Im folgenden Beispiel wird gezeigt, wie mfsampleextension \_ Encryption \_ subsamplemappingsplit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f5147-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="f5147-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5147-115">Requirements</span></span>



| <span data-ttu-id="f5147-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5147-116">Requirement</span></span> | <span data-ttu-id="f5147-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f5147-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5147-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5147-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5147-119">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f5147-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="f5147-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5147-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5147-121">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f5147-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f5147-122">Header</span><span class="sxs-lookup"><span data-stu-id="f5147-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5147-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5147-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5147-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5147-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5147-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f5147-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5147-126">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="f5147-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="f5147-127">MF SampleExtension- \_ Inhalts \_ Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="f5147-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




