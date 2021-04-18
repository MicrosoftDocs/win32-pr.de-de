---
description: Das Längenfeld in einem TLV-Wert gibt die Anzahl der Bytes an, die im Wertfeld codiert sind.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Codierte Länge und Wert Bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354641"
---
# <a name="encoded-length-and-value-bytes"></a><span data-ttu-id="fc124-103">Codierte Länge und Wert Bytes</span><span class="sxs-lookup"><span data-stu-id="fc124-103">Encoded Length and Value Bytes</span></span>

<span data-ttu-id="fc124-104">Das *Längen* Feld in einem TLV-Wert gibt die Anzahl der Bytes an, die im *Wertfeld* codiert sind.</span><span class="sxs-lookup"><span data-stu-id="fc124-104">The *Length* field in a TLV triplet identifies the number of bytes encoded in the *Value* field.</span></span> <span data-ttu-id="fc124-105">Das Feld *Wert* enthält den Inhalt, der zwischen den Computern gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc124-105">The *Value* field contains the content being sent between computers.</span></span> <span data-ttu-id="fc124-106">Wenn das *Wertfeld* weniger als 128 Bytes enthält, ist für das *Längen* Feld nur ein Byte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fc124-106">If the *Value* field contains fewer than 128 bytes, the *Length* field requires only one byte.</span></span> <span data-ttu-id="fc124-107">Bit 7 des *Längen* Felds ist 0 (null), und die verbleibenden Bits identifizieren die Anzahl der Bytes, die gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc124-107">Bit 7 of the *Length* field is zero (0) and the remaining bits identify the number of bytes of content being sent.</span></span> <span data-ttu-id="fc124-108">Wenn das *Wertfeld* mehr als 127 Bytes enthält, ist Bit 7 des *Längen* Felds eins (1), und die restlichen Bits identifizieren die Anzahl der Bytes, die für die Länge benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc124-108">If the *Value* field contains more than 127 bytes, bit 7 of the *Length* field is one (1) and the remaining bits identify the number of bytes needed to contain the length.</span></span> <span data-ttu-id="fc124-109">Beispiele sind in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fc124-109">Examples are shown in the following illustration.</span></span>

![der TLV-Längenbyte](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a><span data-ttu-id="fc124-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc124-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc124-112">DER-Übertragungs Syntax</span><span class="sxs-lookup"><span data-stu-id="fc124-112">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc124-113">Codierte tagbytes</span><span class="sxs-lookup"><span data-stu-id="fc124-113">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



