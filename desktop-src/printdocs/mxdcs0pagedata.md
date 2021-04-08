---
description: Die mxdc \_ S0PAGE \_ Data \_ T-Struktur enthält eine XPS-Dokument Seite, die ohne Verarbeitung an die Microsoft XPS Document Converter-Ausgabedatei (mxdc) übermittelt werden soll.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T-Struktur (mxdc. h)
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
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757741"
---
# <a name="mxdc_s0page_data_t-structure"></a>Mxdc \_ S0PAGE \_ Data \_ T-Struktur

Die **mxdc \_ S0PAGE \_ Data \_ T** -Struktur enthält eine XPS-Dokument Seite, die ohne Verarbeitung an die Microsoft XPS Document Converter-Ausgabedatei (mxdc) übermittelt werden soll.

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

Die Größe des Ausgabepuffers, **bdata**.

</dd> <dt>

**bData**
</dt> <dd>

Die XPS-Dokument Seite.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird an eine [**mxdc- \_ \_ escapeheader- \_ t**](mxdcescapeheader.md) -Struktur angehängt (deren **Opcode** auf mxdcop Set S0PAGE festgelegt ist \_ \_ ), um eine [**mxdc \_ S0PAGE \_ Passthrough- \_ Escape \_ t**](mxdcs0pagepassthroughescape.md) -Struktur zu erstellen. Diese Struktur wird dann an den *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, wenn Sie mit [**mxdc \_ Escape**](mxdc-escape.md) als Escapezeichen aufgerufen wird. Das Ergebnis ist, dass der mxdc die Seite an die Ausgabe übergibt, ohne Sie zu verarbeiten.

Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)liegen.

Die aufrufende Anwendung ist für die Validierung des XML-Codes der XPS-Dokument Seite verantwortlich.

Der Streamingverbrauch ist effizienter, wenn Sie [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit **mxdcop \_ Set \_ S0PAGE \_ Resource** als **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie Sie mit **mxdcop \_ Set \_ S0PAGE** aufzurufen.

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

 

