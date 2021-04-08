---
description: Die mxdc \_ XPS \_ S0PAGE \_ Resource \_ T-Struktur enthält Informationen über eine Ressource, z. b. ein Bild oder eine Schriftart, die einer XPS-Dokument Seite zugeordnet ist und an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei übermittelt werden soll.
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T-Struktur (mxdc. h)
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
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865871"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>Mxdc \_ XPS \_ S0PAGE \_ Resource \_ T-Struktur

Die **mxdc \_ XPS \_ S0PAGE \_ Resource \_ T** -Struktur enthält Informationen über eine Ressource, z. b. ein Bild oder eine Schriftart, die einer XPS-Dokument Seite zugeordnet ist und an die Microsoft XPS Document Converter (mxdc)-Ausgabedatei übermittelt werden soll.

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

Die Gesamtgröße dieser Struktur und der Ressource, auf die Sie verweist.

</dd> <dt>

**dwresourcetype**
</dt> <dd>

Ein Wert vom Typ [**mxdc \_ S0 \_ - \_ Seiten**](mxdcs0pageenums.md) Enumerationswerte, die den Typ der Ressource angeben, z. b. TIFF-Bild oder TrueType-Schriftart.

</dd> <dt>

**szuri**
</dt> <dd>

Der URI der Ressource. Dies darf nicht mehr als 260 Bytes betragen.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Die Größe der Ressource in Bytes.

</dd> <dt>

**bData**
</dt> <dd>

Die Daten der Ressource in einem Bytearray mit einer Größe von 1 + der Größe der Ressource.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird an eine [**mxdc- \_ Escape- \_ Header- \_ t**](mxdcescapeheader.md) -Struktur angehängt (deren **Opcode** auf **mxdcop \_ Set \_ S0PAGERESOURCE** festgelegt ist), um eine [**mxdc \_ S0PAGE \_ Resource Escape- \_ \_ t**](mxdcs0pageresourceescape.md) -Struktur zu erstellen. Die resultierende **mxdc \_ S0PAGE \_ Resource \_ Escape- \_ T** -Struktur wird dann im *lpszindata* -Parameter der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -Funktion übergeben, die mit dem Escapezeichen " [**mxdc \_**](mxdc-escape.md) " aufgerufen wird. Der Effekt besteht darin, die Ressource für die Konvertierung an den mxdc zu senden und in die Ausgabedatei zu schreiben.

Der [**extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) -aufrufsausdruck muss zwischen einem Aufrufen von [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) und einem Aufrufen von " [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage);" liegen. Es können jedoch mehrere derartige Aufrufe zwischen den Aufrufen von **Startpage** und **EndPage** vorhanden sein.

Der Streamingverbrauch ist effizienter, wenn [**Sie extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) mit dem **mxdcop \_ Set \_ S0PAGE \_ Resource** **Opcode** für jede Ressource auf der Seite aufruft, bevor Sie **extescape** mit dem **mxdcop \_ Set \_ S0PAGE** **Opcode** aufgerufen haben.

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

 

