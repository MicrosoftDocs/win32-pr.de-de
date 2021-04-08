---
description: Gibt die eindeutige (nicht verschlüsselte) Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: MFSampleExtension_Encryption_SkipByteBlock-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863971"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a><span data-ttu-id="d67b8-103">\_Skipbyteblock-Attribut für MF SampleExtension-Verschlüsselung \_</span><span class="sxs-lookup"><span data-stu-id="d67b8-103">MFSampleExtension\_Encryption\_SkipByteBlock attribute</span></span>

<span data-ttu-id="d67b8-104">Gibt die eindeutige (nicht verschlüsselte) Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.</span><span class="sxs-lookup"><span data-stu-id="d67b8-104">Specifies the clear (non-encrypted) byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="d67b8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d67b8-105">Data type</span></span>

<span data-ttu-id="d67b8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d67b8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d67b8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d67b8-107">Remarks</span></span>

<span data-ttu-id="d67b8-108">Die Anzahl verschlüsselter Bytes im Teilprobe-Zuordnungs Block wird im Attribut " [ \_ \_ cryptbyteblock" der MF SampleExtension-Verschlüsselung](mfsampleextension-encryption-cryptbyteblock.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="d67b8-108">The number of encrypted bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) attribute.</span></span> <span data-ttu-id="d67b8-109">Wenn keines dieser Attribute vorhanden ist oder den Wert 0 hat, bedeutet dies, dass die Beispiel Daten nicht verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="d67b8-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="d67b8-110">Beide Werte müssen einen Wert ungleich 0 (null), positive Werte aufweisen, oder beide müssen den Wert 0 (null) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d67b8-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="d67b8-111">In Fällen, in denen die Quelle MP4-basiert ist, wird der Wert basierend auf den Werten des \_ standardskip- \_ \_ Byteblocks innerhalb des Felds "Verschlüsselung nachverfolgen" ("tenc") im MP4-Header festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d67b8-111">In cases where the Source is MP4-based, the value is set based off the values of default\_skip\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="d67b8-112">Weitere Informationen finden Sie unter [MF SampleExtension \_ Encryption \_ Protection Schema](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="d67b8-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d67b8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d67b8-113">Requirements</span></span>



| <span data-ttu-id="d67b8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d67b8-114">Requirement</span></span> | <span data-ttu-id="d67b8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d67b8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d67b8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d67b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d67b8-117">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d67b8-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d67b8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d67b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d67b8-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d67b8-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="d67b8-120">Header</span><span class="sxs-lookup"><span data-stu-id="d67b8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d67b8-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d67b8-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




