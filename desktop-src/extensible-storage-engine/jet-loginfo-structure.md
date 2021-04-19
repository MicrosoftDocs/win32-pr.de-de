---
description: 'Weitere Informationen finden Sie hier: JET_LOGINFO Struktur'
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
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106350741"
---
# <a name="jet_loginfo-structure"></a>JET_LOGINFO Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_loginfo-structure"></a>JET_LOGINFO Struktur

Die **JET_LOGINFO** -Struktur gibt strukturierte Informationen über den Satz von Transaktionsprotokoll Dateien zurück, die Teil eines Sicherungsdatei Satzes sein sollten. Die **JET_LOGINFO** Struktur ist der minimale Satz von Informationen, die erforderlich sind, um einen Bereich von Protokollen darzustellen, der mit [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) abgerufen oder für eine feste Wiederherstellung mit [JetExternalRestore2](./jetexternalrestore2-function.md)angegeben wird.

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a>Member

**CBSIZE**

Die Größe der-Struktur in Bytes.

Dieser Member ermöglicht die zukünftige Erweiterung dieser Struktur, während die Abwärtskompatibilität aktiviert wird. Er sollte immer auf sizeof (JET_LOGINFO) festgelegt werden.

**ulgenlow**

Die niedrigste (oder älteste) Protokolldatei Nummer, die wieder hergestellt wird. Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

**ulgenhigh**

Die höchste (oder letzte) Protokolldatei Nummer, die wieder hergestellt wird. Die vollständige Genauigkeit eines langen Zeichens ohne Vorzeichen sollte beibehalten werden, aber in den aktuellen Versionen der Engine ist diese Zahl eine hexadezimale Zahl im Bereich von 0x00000 bis 0xFFFFF. Dies kann sich in zukünftigen Versionen ändern.

**szbasename**

Das Präfix, das zum Benennen der Transaktionsprotokoll Dateien verwendet wird.

Der Wert, der in diesem Member zurückgegeben wird, entspricht immer der-Einstellung für [JET_paramBaseName](./transaction-log-parameters.md) für die-Instanz, die diese Informationen generiert hat.

### <a name="remarks"></a>Bemerkungen

Transaktionsprotokoll Dateien werden nach dem instanzbasisnamen und der Generations Nummer der Protokolldatei benannt. Der Name hat das Format "bbbxxxxx". Angezeigt. BBB entspricht dem Basis Namen für die Protokolldatei und weist immer eine Länge von drei Zeichen auf. Xxxxx entspricht der Generations Nummer der Protokolldatei in 0 (null) und ist immer fünf Zeichen lang. Log ist die Dateierweiterung, die von der-Engine immer an Transaktionsprotokoll Dateien übergeben wird.

Es wird davon abgeraten, diese strukturierten Informationen zu verwenden, da die Anwendung das Benennungs Schema für Transaktionsprotokoll Dateien mit einem Grundkenntnissen kennt. Wenn das Benennungs Schema in Zukunft geändert wird, funktioniert eine solche Anwendung nicht mehr ordnungsgemäß. Es ist zu berücksichtigen, dass sich das Protokoll Format in Zukunft in 8 hexadezimal Ziffern einfügt. Anwendungen sollten stattdessen die explizite Liste der von [jetgetloginfo](./jetgetloginfo-function.md) zurückgegebenen Dateinamen verwenden.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista oder Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008 oder Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_LOGINFO_W</strong> (Unicode) und <strong>JET_LOGINFO_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JetExternalRestore2](./jetexternalrestore2-function.md)  
[Jetgetloginfo](./jetgetloginfo-function.md)  
[JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md)  
[System Parameter](./extensible-storage-engine-system-parameters.md)
