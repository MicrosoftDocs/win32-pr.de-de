---
title: MSAD_ReplCursor-Klasse
description: Stellt eingehende Replikations Zustandsinformationen zu allen Replikaten eines angegebenen Namens Kontexts (NC) bereit.
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor-Klasse Active Directory
- MSAD_ReplCursor Klasse Active Directory, beschrieben
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
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476845"
---
# <a name="msad_replcursor-class"></a>MSAD \_ replcursor-Klasse

Stellt eingehende Replikations Zustandsinformationen zu allen Replikaten eines angegebenen Namens Kontexts (NC) bereit.

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

Die **MSAD \_ replcursor** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSAD \_ replcursor** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Namingcontextdn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den X. 500-Pfad für den namens Kontext (NC) ab, der diesen Cursor enthält.

</dd> <dt>

**Sourcedsadn**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den X. 500-Pfad für den Verzeichnis System-Agent (DSA) ab, der den Quell Domänen Controller (DC) darstellt.

</dd> <dt>

**Sourcedsainvocationid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Aufruf Bezeichner des Ursprungs Servers ab, **dem der Wert** von "".

</dd> <dt>

**Timeoflastsuccess fulsync**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zeitstempel der letzten erfolgreichen Replikations Synchronisierung mit der Quell-DSA ab. Gibt den Zeitpunkt an, zu dem dieser Domänen Controller zuletzt Änderungen am Quell-DSA für diesen NC feststellte.

</dd> <dt>

**"", "".**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft die maximale Update Sequenznummer ab, auf die der Zielserver angeben kann, dass alle Änderungen, die vom angegebenen Server stammen, in den Update Sequenznummern, die kleiner oder gleich dieser Update Sequenznummer sind, aufgezeichnet wurden. Diese Eigenschaft wird zum Filtern von Änderungen verwendet, die der Zielserver bereits auf Replikations Quell Servern angewendet hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Microsoftactivedirectory-Stammverzeichnis<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DS- \_ repl- \_ Cursor**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

