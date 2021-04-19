---
description: ICE42 überprüft, ob Inproc-Server nicht mit den exe-Dateien in der Klassen Tabelle verknüpft sind. Außerdem wird überprüft, ob nur LocalServer-und LocalServer32-Klassen Argumente und definproc-Werte aufweisen.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356253"
---
# <a name="ice42"></a>ICE42

ICE42 überprüft, ob Inproc-Server nicht mit den exe-Dateien in der [Klassen Tabelle](class-table.md)verknüpft sind. Außerdem wird überprüft, ob nur LocalServer-und LocalServer32-Klassen Argumente und definproc-Werte aufweisen.

## <a name="result"></a>Ergebnis

ICE42 gibt einen Fehler aus, wenn in der Klassen Tabelle Inproc-Server mit exe-Dateien verknüpft sind.

## <a name="example"></a>Beispiel

ICE42 würde die folgenden Fehler für das gezeigte Beispiel melden.



| ICE42-Fehler                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die CLSID "{GUID1}" ist ein Inproc-Server, aber die implementierende Komponente "Component1" hat eine exe-Datei ("test.exe") als Schlüsseldatei.                | Es gibt eine ausführbare Datei, die als Inproc-Server angegeben ist. EXE-Dateien können keine Inproc-Server sein.                                                                                                                            |
| Die CLSID "{GUID1}" im Kontext "InprocServer32" weist ein Argument auf. Nur LocalServer-Kontexte können Argumente aufweisen.                              | Entfernen Sie das-Argument, um diesen Fehler zu beheben.                                                                                                                                                                                   |
| Die CLSID "{GUID1}" im Kontext "InprocServer32" gibt einen standardmäßigen InProc-Wert an. Nur LocalServer-Kontexte können standardmäßige INPROC-Werte aufweisen. | Es gibt ein Objekt mit einem standardmäßigen InProc-Wert, der kein Objekt ist, das in den LocalServer-oder LocalServer32-Kontexten ausgeführt wird. Entfernen Sie den deflnproc-Wert, oder ändern Sie den Kontext der-Klasse, um diesen Fehler zu beheben.<br/> |



 

[Klassen Tabelle](class-table.md) (partiell)



| CLSID   | Kontext        | Komponente\_ | Definprochandler | Argument |
|---------|----------------|-------------|------------------|----------|
| GUID1 | InprocServer32 | Component1  | InprocServer     | Gebeut      |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente  | KEYPATH |
|------------|---------|
| Component1 | Datei1   |



 

[Dateitabelle](file-table.md) (partiell)



| File  | Dateiname |
|-------|----------|
| Datei1 | test.exe |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




