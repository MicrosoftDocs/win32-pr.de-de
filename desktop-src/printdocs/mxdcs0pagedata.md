---
description: Die MXDC S0PAGE DATA T-Struktur enthält eine XPS-Dokumentseite, die ohne Verarbeitung an die \_ \_ MXDC-Ausgabedatei \_ (Microsoft XPS Document Converter) übergeben wird.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T -Struktur (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 1ff54325859acef6da136c4bce20286bc7c746d8880d8994ca834213adf57b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776550"
---
# <a name="mxdc_s0page_data_t-structure"></a>MXDC \_ S0PAGE \_ DATA \_ T-Struktur

Die **MXDC \_ S0PAGE \_ DATA \_ T-Struktur** enthält eine XPS-Dokumentseite, die ohne Verarbeitung an die MXDC-Ausgabedatei (Microsoft XPS Document Converter) übergeben wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Die Größe des Ausgabepuffers **bData.**

</dd> <dt>

**bData**
</dt> <dd>

Die XPS-Dokumentseite.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird an eine [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur**](mxdcescapeheader.md) angefügt (deren **opCode** auf MXDCOP SET S0PAGE festgelegt ist), um eine \_ \_ [**MXDC \_ S0PAGE \_ PASSTHROUGH ESCAPE \_ \_ T-Struktur**](mxdcs0pagepassthroughescape.md) zu erstellen. Diese Struktur wird dann an den *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben, wenn sie mit [**MXDC \_ ESCAPE**](mxdc-escape.md) als Escape-Element aufgerufen wird. Das Ergebnis ist, dass der MXDC die Seite an die Ausgabe übergibt, ohne sie zu verarbeiten.

Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage liegen.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)

Die aufrufende Anwendung ist für die Validierung des XML-Code der XPS-Dokumentseite verantwortlich.

Die Streamingnutzung ist effizienter, wenn Sie [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** als **opCode** für jede Ressource auf der Seite aufrufen, bevor Sie sie mit **MXDCOP \_ SET \_ S0PAGE aufrufen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[GDI-Drucker-Escapefunktionen](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

