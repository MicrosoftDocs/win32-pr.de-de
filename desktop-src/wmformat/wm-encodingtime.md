---
title: WM/encodingtime
description: Das WM/encodingtime-Attribut enthält einen Zeitstempel der Zeit, zu der der Inhalt codiert wurde.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- WM/encodingtime Windows Media-Format
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038177"
---
# <a name="wmencodingtime"></a>WM/encodingtime

Das **WM/encodingtime-** Attribut enthält einen Zeitstempel der Zeit, zu der der Inhalt codiert wurde.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmencodingtime

## <a name="data-type"></a>Datentyp

**FILETIME** (**WMT- \_ Typ \_ QWORD**)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut verwendet einen FILETIME-Wert. dabei handelt es sich um einen 64-Bit-Wert, der die Anzahl der seit dem 1. Januar 1601 verstrichenen 100-Nanosecond-Zeiteinheiten darstellt. Weitere Informationen zur FILETIME finden Sie im Abschnitt Windows-System Informationen des Platform SDK.

Dabei handelt es sich nicht um ein codiertes Attribut. Sie müssen es manuell festlegen, wenn Sie es in Ihre Dateien einschließen möchten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




