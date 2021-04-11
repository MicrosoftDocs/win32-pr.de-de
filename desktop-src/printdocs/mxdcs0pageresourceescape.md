---
description: Die mxdc \_ S0PAGE \_ Resource \_ Escape \_ t-Struktur ist eine mxdc-Escape-Header-t-Struktur, die \_ \_ \_ mit einer mxdc \_ XPS \_ S0PAGE \_ Resource \_ T-Struktur verkettet ist.
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: MXDC_S0PAGE_RESOURCE_ESCAPE_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215970"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>Mxdc \_ S0PAGE \_ Resource \_ Escape- \_ T-Struktur

Die **mxdc \_ S0PAGE \_ Resource \_ Escape \_ t** -Struktur ist eine [**mxdc- \_ Escape-Header- \_ \_ t**](mxdcescapeheader.md) -Struktur, die mit einer [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur verkettet ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>Member

<dl> <dt>

**mxdcescape**
</dt> <dd>

Eine [**mxdc- \_ Escape- \_ Header- \_ T**](mxdcescapeheader.md) -Struktur, deren **Opcode** -Member auf mxdcop \_ Set S0PAGE Resource festgelegt ist \_ \_ .

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Eine [**mxdc \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) -Struktur, die eine Ressource (z. b. eine Schriftart oder Bilddatei) auf einer XPS-Dokument Seite darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn diese Funktion mit dem Escapezeichen " [**mxdc \_**](mxdc-escape.md) " aufgerufen wird und der **Opcode** -Member der [**mxdc- \_ Escape-Header- \_ \_ T**](mxdcescapeheader.md) -Struktur **mxdcop \_ Set \_ S0PAGE \_ Resource** ist. Das Ergebnis ist eine Seiten Ressource, die an den mxdc gesendet wird.

Weisen Sie der Escapesequenz wie unten gezeigt den Speicher zu, legen Sie die Felder nach Bedarf fest, und nennen Sie dann [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von " [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage);" liegen. zwischen den Aufrufen von **Startpage** und **EndPage** können jedoch mehr als einer dieser Aufrufe vorhanden sein.

Der Streamingverbrauch ist effizienter, wenn [**Sie extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem **mxdcop \_ Set \_ S0PAGE \_ Resource** **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie **extescape** mit dem **mxdcop \_ Set \_ S0PAGE**  **Opcode** aufgerufen haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[Escapefunktionen für GDI-Drucker](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**Extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**mxdc-Escapezeichen \_**](mxdc-escape.md)
</dt> </dl>

 

