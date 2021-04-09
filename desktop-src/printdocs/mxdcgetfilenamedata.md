---
description: Die mxdc \_ get \_ filename \_ Data \_ T-Struktur enthält den vollständigen Pfad und den Dateinamen einer Microsoft XPS Document Converter (mxdc)-Ausgabedatei.
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T-Struktur (mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864963"
---
# <a name="mxdc_get_filename_data_t-structure"></a>Mxdc \_ get \_ filename \_ Data \_ T-Struktur

Die **mxdc \_ get \_ filename \_ Data \_ T** -Struktur enthält den vollständigen Pfad und den Dateinamen einer Microsoft XPS Document Converter (mxdc)-Ausgabedatei.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Member

<dl> <dt>

**cboutput**
</dt> <dd>

Die Größe des Ausgabepuffers, **wszdata**.

</dd> <dt>

**wszdata**
</dt> <dd>

Der voll qualifizierte Pfad und Dateiname der Ausgabedatei.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zurückgegeben, wenn Sie mit dem Escapezeichen für [**\_ mxdc**](mxdc-escape.md) aufgerufen wird und die im *lpszindata* -Parameter übergebenen [**mxdc- \_ escapeheader- \_ \_ T**](mxdcescapeheader.md) -Struktur den **Opcode** auf **mxdcop \_ get \_ filename** festgelegt ist.

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

 

