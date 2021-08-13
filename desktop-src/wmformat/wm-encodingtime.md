---
title: WM/EncodingTime
description: Das WM/EncodingTime-Attribut enthält einen Zeitstempel der Zeit, zu der der Inhalt codiert wurde.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- WM/EncodingTime-Windows-Medienformat
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c76de789bd6ca88a9bbc2f3bb68381b3816524a07cbf97dc1a35b2526179a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431839"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

Das **WM/EncodingTime-Attribut** enthält einen Zeitstempel der Zeit, zu der der Inhalt codiert wurde.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMEncodingTime

## <a name="data-type"></a>Datentyp

**FILETIME** (**WMT \_ TYPE \_ QWORD**)

## <a name="remarks"></a>Hinweise

Dieses Attribut verwendet einen FILETIME-Wert, bei dem es sich um einen 64-Bit-Wert handelt, der die Anzahl der 100-Nanosekunden-Zeiteinheiten darstellt, die seit dem 1. Januar 1601 verstrichen sind. Weitere Informationen zu FILETIME finden Sie im abschnitt Windows Systeminformationen des Platform SDK.

Dies ist kein codiertes Attribut. Sie müssen sie manuell festlegen, wenn Sie sie in Ihre Dateien ein-/ausdingen möchten.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




