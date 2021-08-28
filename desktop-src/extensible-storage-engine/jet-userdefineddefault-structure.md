---
description: 'Weitere Informationen finden Sie unter: JET_USERDEFINEDDEFAULT Struktur'
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
ms.openlocfilehash: a8e5cfe4fadf0dead2e11787255089d251a98f67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479306"
---
# <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT Struktur


_**Gilt für:** Windows | Windows Server_

## <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT Struktur

Die **JET_USERDEFINEDDEFAULT-Struktur** wird in Verbindung mit JET_bitColumnUserDefinedDefault angegeben, um einer neuen Spalte einen Standardwert zu geben, der mithilfe eines Rückrufs bestimmt wird. Diese Technik kann verwendet werden, um berechnete Spalten zu implementieren.

**Windows XP:** Die **JET_USERDEFINEDDEFAULT-Struktur** wird in Windows XP eingeführt.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Member

**szCallback**

Der Exportname der Funktion, die den Rückruf im Modulfunktionsformat \! implementiert.

Der Rückruf wird als Teil des Spaltenschemas beibehalten. Die tatsächliche ausführbare Hostdatei und der Exportname der Funktion müssen beibehalten werden, um die Suche nach der tatsächlichen Adresse der Funktion zur Laufzeit zu ermöglichen.

Der Modulname ist der Name der Hostbinärdatei, die die Funktion enthält. Der Funktionsname ist der Name des Exports für diese Funktion. Diese beiden Informationen werden von der Datenbank-Engine zur Laufzeit verwendet, um die echte Adresse des Rückrufs zu ermitteln, indem ein [LoadLibrary-Aufruf](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) für den Modulnamen gefolgt von einem [GetProcAddress-Aufruf](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) für den Funktionsnamen ausgeführt wird.

Wenn der Rückruf beispielsweise in einer DLL namens MyCallback.DLL implementiert wurde und diese DLL in C: MyApplication gespeichert wurde und die Funktion, die den Rückruf implementiert, aus der DLL als UserDefinedDefaultCallback exportiert wurde, wäre die erforderliche Zeichenfolge \\ "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Hinweis:**  Embedded " \! " " -Zeichen im Modulteil des Rückrufnamens werden nicht unterstützt.

Es wird dringend empfohlen, einen Rückrufnamen zu verwenden, der keine Funktion der Hostarchitektur ist. Verwenden Sie beispielsweise keine Exporte, die als stdcall ( ) verziert sind, da diese Aufrufkonvention nur auf UserDefinedDefaultCallback@32 x86-Computern unterstützt wird. Wenn ein solcher Rückruf verwendet wird, kann die Datenbank nur auf einem x86-Computer verwendet werden. In diesem Fall sollte ein Alias verwendet werden, um einen plattformunabhängigen Export zu erstellen.

Es wird dringend empfohlen, den vollständigen Pfad des Modulnamens zu verwenden, der den Rückruf implementieren soll. Wenn ein relativer Pfad verwendet wird, kann der Prozess, der die Datenbank hosten, anfällig für Angriffe durch eine nicht autorisierte Binärdatei sein.

Die Anwendung sollte nur vertrauenswürdige Rückrufe an die Datenbank-Engine übergeben. Die Datenbank-Engine geladen die Binärdatei, um zu überprüfen, ob sie vorhanden ist, wenn die zugeordnete Spalte erstellt wird. Wenn der Pfad zur Binärdatei nicht überprüft wird oder als vertrauenswürdig eingestuft wird, kann er den Prozess angreifen, der die Datenbank hosten soll.

**pbUserData**

Ein eigenständiger Block von benutzerdefinierten Daten, die beim Aufrufen an den Rückruf übergeben werden sollen. Der bereitgestellte Datenblock wird als Teil des Spaltenschemas beibehalten. Daher muss der Datenblock vollständig in sich geschlossen sein und darf nicht auf Daten verweisen, die außerhalb des Gültigkeitsbereichs der Datenbank sind.

Wenn **pbUserData** 0 (null) ist, wird der **Wert von cbUserData** ignoriert. In diesem Fall werden keine benutzerdefinierten Daten an den Rückruf übergeben, wenn sie aufgerufen werden.

**cbUserData**

Weitere Informationen **finden Sie unter pbUserData.**

**szDependantColumns**

Für die zukünftige Verwendung reserviert.

Dieser Member sollte immer auf NULL festgelegt werden.

### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | | <p><strong>Unicode</strong></p> | <p>Wird als <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) <strong>und</strong> JET_ USERDEFINEDDEFAULT_A (ANSI) implementiert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
