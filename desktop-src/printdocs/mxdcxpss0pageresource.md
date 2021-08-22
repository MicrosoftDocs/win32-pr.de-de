---
description: Die MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T-Struktur enthält Informationen über eine Ressource, z. B. ein Bild oder eine Schriftart, die einer XPS-Dokumentseite zugeordnet ist und an die Ausgabedatei des Microsoft XPS-Dokumentkonverters (MXDC) übergeben werden soll.
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T-Struktur (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 21035a99b6237c481a5b7560f469086ef2960d655ba32582ed273edb48910ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971179"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T-Struktur

Die **MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T-Struktur** enthält Informationen über eine Ressource, z. B. ein Bild oder eine Schriftart, die einer XPS-Dokumentseite zugeordnet ist und an die Ausgabedatei des Microsoft XPS-Dokumentkonverters (MXDC) übergeben werden soll.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Die Gesamtgröße dieser Struktur und die Ressource, auf die sie verweist.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Ein Wert vom Typ [**MXDC \_ S0 \_ PAGE \_ ENUMS,**](mxdcs0pageenums.md) der den Typ der Ressource angibt, z. B. TIFF-Image oder TrueType-Schriftart.

</dd> <dt>

**szUri**
</dt> <dd>

Der URI der Ressource. Dies darf nicht mehr als 260 Bytes sein.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Die Größe der Ressource in Bytes.

</dd> <dt>

**bData**
</dt> <dd>

Die Daten der Ressource in einem Bytearray mit der Größe 1 und der Größe der Ressource.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird an eine [**MXDC \_ ESCAPE HEADER \_ \_ T-Struktur**](mxdcescapeheader.md) angefügt (deren **opCode** auf **MXDCOP \_ SET \_ S0PAGERESOURCE** festgelegt ist), um eine [**MXDC \_ S0PAGE \_ RESOURCE ESCAPE \_ \_ T-Struktur**](mxdcs0pageresourceescape.md) zu erstellen. Die resultierende **MXDC \_ S0PAGE \_ RESOURCE ESCAPE \_ \_ T-Struktur** wird dann im *lpszInData-Parameter* der [**ExtEscape-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) übergeben, die mit dem [**MXDC \_ ESCAPE-Escapewert**](mxdc-escape.md) aufgerufen wird. Der Effekt besteht darin, die Ressource zur Konvertierung an das MXDC zu senden und in die Ausgabedatei zu schreiben.

Der Aufruf von [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) muss zwischen einem Aufruf von [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufruf von [**EndPage erfolgen.**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) zwischen den Aufrufen von **StartPage** und **EndPage** kann jedoch mehr als ein solcher Aufruf vorhanden sein.

Die Streamingnutzung ist effizienter, wenn Sie [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** **opCode** für jede Ressource auf der Seite aufrufen, bevor Sie **ExtEscape** mit dem **MXDCOP \_ SET \_ S0PAGE** **opCode** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                    |
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

 

