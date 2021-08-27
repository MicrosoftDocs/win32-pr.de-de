---
description: 'Weitere Informationen finden Sie unter: JET_LOGINFO Struktur'
title: JET_LOGINFO Struktur
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f5619211a5fc76bb080b81b22c08c9e369abf93
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983163"
---
# <a name="jet_loginfo-structure"></a>JET_LOGINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_loginfo-structure"></a>JET_LOGINFO Struktur

Die **JET_LOGINFO** struktur gibt strukturierte Informationen über den Satz von Transaktionsprotokolldateien zurück, die Teil eines Sicherungsdateisets sein sollten. Die **JET_LOGINFO-Struktur** ist der minimale Satz von Informationen, die erforderlich sind, um einen Bereich von Protokollen anzugeben, der mit [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) abgerufen oder für eine harte Wiederherstellung mit [JetExternalRestore2](./jetexternalrestore2-function.md)angegeben wird.

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Member

**cbSize**

Die Größe der -Struktur in Bytes.

Dieser Member ermöglicht eine zukünftige Erweiterung dieser Struktur bei gleichzeitiger Aktivierung der Abwärtskompatibilität. Sie sollte immer auf sizeof( JET_LOGINFO ) festgelegt werden.

**ulGenLow**

Die niedrigste (oder älteste) Protokolldateinummer, die wiederhergestellt wird. Die vollständige Genauigkeit eines unsignierten long-Werts sollte beibehalten werden, aber in aktuellen Versionen der Engine ist diese Zahl eine Hexadezimalzahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

**ulGenHigh**

Die höchste (oder letzte) Protokolldateinummer, die wiederhergestellt wird. Die vollständige Genauigkeit eines unsignierten long-Werts sollte beibehalten werden, aber in aktuellen Versionen der Engine ist diese Zahl eine Hexadezimalzahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

**szBaseName**

Das Präfix, das zum Benennen der Transaktionsprotokolldateien verwendet wird.

Der Wert, der in diesem Member zurückgegeben [](./transaction-log-parameters.md) wird, entspricht immer der Einstellung für JET_paramBaseName instanz, die diese Informationen generiert hat.

### <a name="remarks"></a>Bemerkungen

Transaktionsprotokolldateien werden entsprechend dem Basisnamen der Instanz und der Generierungsnummer der Protokolldatei benannt. Der Name hat das Format BBBXXXXX. PROTOKOLL. BBB entspricht dem Basisnamen für die Protokolldatei und hat immer eine Länge von drei Zeichen. XXXXX entspricht der Generierungsnummer der Protokolldatei in hexadezimaler Form ohne Auffüllen und hat immer eine Länge von fünf Zeichen. LOG ist die Dateierweiterung, die von der Engine immer an Transaktionsprotokolldateien gegeben wird.

Von der Verwendung dieser strukturierten Informationen wird abgeraten, da die Anwendung dieses Benennungsschema für Transaktionsprotokolldateien nicht kennen muss. Wenn sich das Benennungsschema in Zukunft ändert, funktioniert eine solche Anwendung nicht mehr ordnungsgemäß. Es ist vorstellbar, dass sich das Protokollformat ändert, um in Zukunft acht Hexadezimalziffern zu integrieren. Anwendungen sollten stattdessen die explizite Liste der dateinamen verwenden, die von [JetGetLogInfo zurückgegeben](./jetgetloginfo-function.md) werden.

### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 
| <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_LOGINFO_W</strong> (Unicode) und JET_LOGINFO_A (ANSI) implementiert. <strong></strong></p> | 



### <a name="see-also"></a>Weitere Informationen

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[Systemparameter](./extensible-storage-engine-system-parameters.md)
