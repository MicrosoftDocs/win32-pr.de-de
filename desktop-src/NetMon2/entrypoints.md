---
description: Die entryPoints-Struktur definiert die Einstiegspunkte für die Exportfunktionen, die von Netzwerkmonitor zum Ausführen des Parsers verwendet werden.
ms.assetid: e2ac118d-e04b-489f-877f-84cc9888f8af
title: EntryPoints-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ENTRYPOINTS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3eebee878cd907ee20674224a969c82038f4ac6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958732"
---
# <a name="entrypoints-structure"></a>EntryPoints-Struktur

Die **entryPoints** -Struktur definiert die Einstiegspunkte für die Exportfunktionen, die von Netzwerkmonitor zum Ausführen des Parsers verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct __ENTRYPOINTS {
  REGISTER         Register;
  DEREGISTER       Deregister;
  RECOGNIZEFRAME   RecognizeFrame;
  ATTACHPROPERTIES AttachProperties;
  FORMATPROPERTIES FormatProperties;
} ENTRYPOINTS, *LPENTRYPOINTS;
```



## <a name="members"></a>Member

<dl> <dt>

**Registrieren**
</dt> <dd>

Ein Zeiger auf die Implementierung der [*Register-expertenfunktion*](register-expert.md) .

</dd> <dt>

**Registrierung aufheben**
</dt> <dd>

Ein Zeiger auf die Implementierung der [**deregiester**](deregister.md) -Funktion.

</dd> <dt>

**Erkenzeframe**
</dt> <dd>

Ein Zeiger auf die Implementierung der Funktion " [**Erkennungs Frame**](recognizeframe.md) -Export".

</dd> <dt>

**Attachproperties**
</dt> <dd>

Ein Zeiger auf die Implementierung der " [**attachproperties**](attachproperties.md) "-Exportfunktion.

</dd> <dt>

**Formatproperties**
</dt> <dd>

Ein Zeiger auf die Implementierung der [**formatproperties**](formatproperties.md) -Exportfunktion.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Funktion "** **entryPoints" verwendet die entryPoints** -Struktur, um Zeiger auf Netzwerkmonitor bereitzustellen. Die Zeiger müssen in der im vorherigen Members-Abschnitt identifizierten Reihenfolge angegeben werden.

Die [**formatproperties**](formatproperties.md) -Funktion muss nicht implementiert werden, wenn Netzwerkmonitor die Protokolldaten niemals anzeigt. Beispielsweise muss **formatproperties** nicht implementiert werden, wenn eine Export Anwendung die Ausgabe des Parsers verwendet und Netzwerkmonitor die Ausgabe nicht anzeigt.



| Für Informationen zu                                        | Siehe                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                  |
| Zur Implementierung von **DllMain**  gehört ein Beispiel.        | [Implementieren von DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Attachproperties](attachproperties.md)
</dt> <dt>

["Kreateprotocol"](createprotocol.md)
</dt> <dt>

[Registrierung aufheben](deregister.md)
</dt> <dt>

[Formatproperties](formatproperties.md)
</dt> <dt>

[Erkenzeframe](recognizeframe.md)
</dt> <dt>

[Registrieren](register-parser.md)
</dt> </dl>

 

 




