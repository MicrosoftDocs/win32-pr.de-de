---
title: OPAQUECOMMAND-Struktur
description: Die OPAQUECOMMAND-Struktur enthält Daten für Befehle, die über Windows Media Geräte-Manager an ein Gerät übergeben werden, aber nicht von Windows Media Geräte-Manager verarbeitet werden sollen.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- OPAQUECOMMAND-Strukturfenster Media Geräte-Manager
- struktur windows Media Geräte-Manager
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d3f0b94146262c480e7e510497111bf82f0c020001717cb0000ee4a88df440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904010"
---
# <a name="opaquecommand-structure"></a>OPAQUECOMMAND-Struktur

Die **OPAQUECOMMAND-Struktur** enthält Daten für Befehle, die über Windows Media-Geräte-Manager an ein Gerät übergeben werden, aber nicht von Windows Media Geräte-Manager verarbeitet werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**guidCommand**
</dt> <dd>

**GUID,** die den angeforderten Befehl darstellt.

</dd> <dt>

**dwDataLen**
</dt> <dd>

Länge der Daten, auf die *pData* verweist, in Bytes.

</dd> <dt>

**Pdata**
</dt> <dd>

Daten, die zum Ausführen des Befehls erforderlich sind, und/oder daten, die vom Befehl zurückgegeben werden.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Dieser Nachrichtenauthentifizierungscode (MAC) sollte den **guidCommand-Member,** die Daten, auf die *pdwDataLen* verweist, und die Daten, auf die *pData-Punkte* (falls vorhanden) enthalten. Wenn *pData* **NULL** ist, darf es nicht im MAC enthalten sein. WMDM \_ MAC LENGTH ist als \_ 20 definiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMDSPDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**IMDSPStorage::SendOpaqueCommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**IWMDMDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





