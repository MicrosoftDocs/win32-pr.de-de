---
description: Die MXDC S0PAGE PASSTHROUGH ESCAPE T-Struktur ist eine MXDC ESCAPE HEADER T-Struktur, die mit einer \_ \_ \_ \_ \_ \_ \_ MXDC \_ S0PAGE \_ DATA \_ T-Struktur verkettet ist.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T -Struktur (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: f8e0a46766f38aec16758a1efc9c0cbc775c2131b1279dcc47f92ed41e77c0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099054"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>MXDC \_ S0PAGE \_ PASSTHROUGH \_ ESCAPE \_ T-Struktur

Die **MXDC \_ S0PAGE \_ PASSTHROUGH \_ ESCAPE \_ T-Struktur** ist eine [**MXDC ESCAPE HEADER \_ \_ \_ T-Struktur,**](mxdcescapeheader.md) die mit einer [**MXDC \_ S0PAGE \_ DATA \_ T-Struktur verkettet**](mxdcs0pagedata.md) ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>Member

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Eine [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur,**](mxdcescapeheader.md) deren **opCode-Member** auf **MXDCOP \_ SET \_ S0PAGE festgelegt ist.**

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Eine [**MxdcS0PageData-Struktur,**](mxdcs0pagedata.md) die eine XPS-Dokumentseite darstellt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird im *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben, wenn sie mit dem ESCAPE-Escape-Element [**MXDC \_**](mxdc-escape.md) aufgerufen wird und der **opCode-Member** der [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur**](mxdcescapeheader.md) **MXDCOP \_ SET \_ S0PAGE** ist. Das Ergebnis ist, dass der Microsoft XML Document Converter (MXDC) die Seite an den Drucker weitergibt, ohne sie zu verarbeiten.

Ordnen Sie arbeitsspeicher für das Escape-Escapefeld zu, wie unten gezeigt, legen Sie die Felder nach Bedarf fest, und rufen Sie [**dann ExtEscape auf.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage liegen.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)

Die aufrufende Anwendung ist für die Validierung des XML-Code der XPS-Dokumentseite verantwortlich.

Die Streamingnutzung ist effizienter, wenn Sie [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** als **opCode** für jede Ressource auf der Seite aufrufen, bevor Sie sie mit **MXDCOP \_ SET \_ S0PAGE aufrufen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

