---
description: Die MXDC GET FILENAME DATA T-Struktur enthält den vollständigen Pfad und Dateinamen einer \_ \_ \_ \_ MXDC-Ausgabedatei (Microsoft XPS Document Converter).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T -Struktur (Mxdc.h)
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
ms.openlocfilehash: ef0b29590b4a9080e943fae5c3e78fb18a99232a2a531a80b63b303b28c2bea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948340"
---
# <a name="mxdc_get_filename_data_t-structure"></a>MXDC \_ GET \_ FILENAME DATA \_ \_ T-Struktur

Die **MXDC \_ GET \_ FILENAME DATA \_ \_ T-Struktur** enthält den vollständigen Pfad und Dateinamen einer MXDC-Ausgabedatei (Microsoft XPS Document Converter).

## <a name="syntax"></a>Syntax


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Member

<dl> <dt>

**cbOutput**
</dt> <dd>

Die Größe des Ausgabepuffers **wszData.**

</dd> <dt>

**wszData**
</dt> <dd>

Der vollqualifizierte Pfad und Dateiname der Ausgabedatei.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) zurückgegeben, wenn sie mit dem ESCAPE-Escape-Element [**MXDC \_**](mxdc-escape.md) aufgerufen wird und für die [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur,**](mxdcescapeheader.md) die im *lpszInData-Parameter* übergeben wird, der **opCode** auf **MXDCOP GET FILENAME festgelegt \_ \_ ist.**

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

 

