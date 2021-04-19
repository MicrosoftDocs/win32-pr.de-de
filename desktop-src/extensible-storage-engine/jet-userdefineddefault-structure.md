---
description: 'Weitere Informationen finden Sie hier: JET_USERDEFINEDDEFAULT Struktur'
title: JET_USERDEFINEDDEFAULT Struktur
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355387"
---
# <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT Struktur

Die **JET_USERDEFINEDDEFAULT** Struktur wird in Verbindung mit JET_bitColumnUserDefinedDefault angegeben, um einer neuen Spalte einen Standardwert zu übergeben, der mithilfe eines Rückrufs bestimmt wird. Diese Technik kann zum Implementieren berechneter Spalten verwendet werden.

**Windows XP:** Die **JET_USERDEFINEDDEFAULT** Struktur wird in Windows XP eingeführt.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Member

**szcallback**

Der Export Name der Funktion, die den Rückruf im Format "Modul \! Funktion" implementiert.

Der Rückruf wird als Teil des Spalten Schemas beibehalten. Die tatsächliche ausführbare Hostdatei und der Export Name der Funktion müssen persistent gespeichert werden, um die Suche nach der tatsächlichen Adresse der Funktion zur Laufzeit zu ermöglichen.

Der Modulname ist der Name der Host Binärdatei, die die Funktion enthält. Der Name der Funktion ist der Name des Exports für diese Funktion. Diese beiden Informationen werden von der Datenbank-Engine zur Laufzeit verwendet, um die tatsächliche Adresse des Rückrufs zu ermitteln, indem Sie einen [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Befehl für den Modulnamen gefolgt von einem [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Aufrufs für den Funktionsnamen ausführen.

Wenn der Rückruf z. b. in einer DLL mit dem Namen MyCallback.DLL implementiert wurde und diese DLL in C: \\ MyApplication gespeichert wurde und die Funktion, die den Rückruf implementiert, als userdefineddefaultcallback von der dll exportiert wurde, lautet die erforderliche Zeichenfolge "C: \\ MyApplication \\MyCallback.DLL\! userdefineddefaultcallback".

**Hinweis**  Eingebettet " \! " Zeichen im Modulteil des Rückruf namens werden nicht unterstützt.

Es wird dringend empfohlen, einen Rückruf Namen zu verwenden, der keine Funktion der Host Architektur ist. Verwenden Sie beispielsweise keine als stdcall () ergänzten Exporte, UserDefinedDefaultCallback@32 da diese Aufruf Konvention nur auf x86-Computern unterstützt wird. Wenn ein solcher Rückruf verwendet wurde, konnte die Datenbank nur auf einem x86-Computer verwendet werden. Ein Alias sollte in diesem Fall verwendet werden, um einen plattformunabhängigen Export vorzunehmen.

Es wird dringend empfohlen, dass Sie den vollständigen Pfad des Modul namens verwenden, der den Rückruf implementiert. Wenn ein relativer Pfad verwendet wird, kann der Prozess, der die Datenbank gehostet, anfällig für Angriffe durch eine nicht autorisierte Binärdatei sein.

Die Anwendung sollte nur vertrauenswürdige Rückrufe an die Datenbank-Engine übergeben. Die Datenbank-Engine lädt die Binärdatei, um deren vorhanden sein zu überprüfen, wenn die zugehörige Spalte erstellt wird. Wenn der Pfad zur Binärdatei nicht überprüft wird oder bekannt ist, dass Sie vertrauenswürdig ist, könnte Sie den Prozess angreifen, der die Datenbank gehostet.

**pbuserdata**

Ein eigenständiger Block von benutzerdefinierten Daten, die beim Aufrufen an den Rückruf übermittelt werden sollen. Der bereitgestellte Datenblock wird als Teil des Spalten Schemas beibehalten. Folglich muss der Datenblock vollständig eigenständig sein und kann nicht auf Daten verweisen, die sich außerhalb des Gültigkeits Bereichs der Datenbank befinden.

Wenn **pbuserdata** NULL ist, wird der Wert von **cbUserData** ignoriert. In diesem Fall werden keine benutzerdefinierten Daten an den Rückruf übermittelt, wenn Sie aufgerufen werden.

**cbUserData**

Siehe **pbuserdata**.

**szdependantcolumns**

Für die zukünftige Verwendung reserviert.

Dieser Member sollte immer auf NULL festgelegt werden.

### <a name="requirements"></a>Anforderungen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>In "ESENT. h" deklariert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Wird als <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) und <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI) implementiert.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Weitere Informationen

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
