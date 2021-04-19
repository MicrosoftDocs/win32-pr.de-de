---
title: Opaquecommand-Struktur
description: Die opaquecommand-Struktur enthält Daten für Befehle, die über Windows Media Device Manager an ein Gerät übermittelt werden, aber nicht von Windows Media Device Manager verarbeitet werden sollen.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Opaquecommand-Struktur Windows Media Device Manager
- Struktur der Windows Media-Device Manager
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
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361507"
---
# <a name="opaquecommand-structure"></a>Opaquecommand-Struktur

Die **opaquecommand** -Struktur enthält Daten für Befehle, die über Windows Media Device Manager an ein Gerät übermittelt werden, aber nicht von Windows Media Device Manager verarbeitet werden sollen.

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

**guidcommand**
</dt> <dd>

**GUID** , die den angeforderten Befehl darstellt.

</dd> <dt>

**dwdatalen**
</dt> <dd>

Länge der Daten, auf die *pData* verweist (in Bytes).

</dd> <dt>

**pData**
</dt> <dd>

Die zum Ausführen des Befehls erforderlichen Daten und/oder Daten, die vom Befehl zurückgegeben werden.

</dd> <dt>

**abmac \[ 20\]**
</dt> <dd>

Dieser Nachrichten Authentifizierungscode (Mac) sollte den **guidcommand** -Member, die Daten, auf die *pdwdatalen* verweist, und die Daten, auf die *pData* verweist, ggf. einschließen. Wenn *pData* **null** ist, darf es nicht in den Mac eingeschlossen werden. Die Länge von WMDM \_ Mac \_ ist als 20 definiert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imdspdevice:: sendopaquecommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**Imdspstorage:: sendopaquecommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**Iwmdmdevice:: sendopaquecommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**Iwmdmstorage:: sendopaquecommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





