---
title: Vbrpeak
description: Das vbrpeak-Attribut enthält die höchste momentane Bitrate in einem VBR-codierten Stream (Variable Bitrate).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- Vbrmaximum Windows Media-Format
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038080"
---
# <a name="vbrpeak"></a>Vbrpeak

Das **vbrpeak** -Attribut enthält die höchste momentane Bitrate in einem VBR-codierten Stream (Variable Bitrate).

## <a name="global-constant"></a>Globale Konstante

g \_ wszvbrpeak

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Beim Zugriff auf die **IWMHeaderInfo3** -Schnittstelle des Writer-Objekts können Sie diesen Wert hinzufügen oder ändern. In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt.

Der Writer schreibt automatisch einen **vbrpeak** -Wert für jeden VBR-Stream.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




