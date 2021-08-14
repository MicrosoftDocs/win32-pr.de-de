---
title: MSAD_ReplCursor-Klasse
description: Stellt eingehende Replikationsstatusinformationen zu allen Replikaten eines bestimmten Namenskontexts (NC) bereit.
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor Active Directory-Klasse
- MSAD_ReplCursor Active Directory-Klasse beschrieben
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c001adf774321ba61e232298d070fb4a29d4b3f0740dd8ef900ff4ea0b4cb83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186065"
---
# <a name="msad_replcursor-class"></a>MSAD \_ ReplCursor-Klasse

Stellt eingehende Replikationsstatusinformationen zu allen Replikaten eines bestimmten Namenskontexts (NC) bereit.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a>Member

Die **MSAD \_ ReplCursor-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ ReplCursor-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den X.500-Pfad für den Namenskontext (NC) ab, der diesen Cursor enthält.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X.500-Pfad für den Verzeichnissystem-Agent (Directory System Agent, DSA) ab, der den Quelldomänencontroller (DC) darstellt.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Aufrufbezeichner des Ursprungsservers ab, dem der **USNAttributeFilter** entspricht.

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel der letzten erfolgreichen Replikationssynchronisierung mit dem Quell-DSA ab. Gibt den Zeitpunkt an, zu dem dieser Domänencontroller zuletzt Änderungen am Quell-DSA für diesen NC vorgenommen hat.

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die maximale Updatesequenznummer ab, für die der Zielserver angeben kann, dass er alle Änderungen aufgezeichnet hat, die vom angegebenen Server stammen, wenn die Updatesequenznummern kleiner oder gleich dieser Updatesequenznummer sind. Diese Eigenschaft wird verwendet, um Änderungen zu filtern, die der Zielserver bereits auf Replikationsquellserver angewendet hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DS \_ REPL \_ CURSOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

