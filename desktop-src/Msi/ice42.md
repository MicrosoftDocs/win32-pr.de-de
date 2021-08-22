---
description: ICE42 überprüft, ob InProc-Server nicht mit EXE-Dateien in der Class-Tabelle verknüpft sind. Außerdem wird überprüft, ob nur die Klassen LocalServer und LocalServer32 Über Argumente und DefInProc-Werte verfügen.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b913b92d82ad25a9722b289596f6b51940bbade55b5e544ebf636051e21b3ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581070"
---
# <a name="ice42"></a>ICE42

ICE42 überprüft, ob InProc-Server nicht mit EXE-Dateien in der [Klassentabelle](class-table.md)verknüpft sind. Außerdem wird überprüft, ob nur die Klassen LocalServer und LocalServer32 Über Argumente und DefInProc-Werte verfügen.

## <a name="result"></a>Ergebnis

ICE42 gibt einen Fehler aus, wenn InProc-Server mit EXE-Dateien in der Class-Tabelle verknüpft sind.

## <a name="example"></a>Beispiel

ICE42 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE42-Fehler                                                                                                                             | Beschreibung                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID "{GUID1}" ist ein InProc-Server, aber die implementierende Komponente "Component1" verfügt über eine EXE -Datei ('test.exe') als KeyFile.                | Es ist eine ausführbare Datei als InProc-Server angegeben. EXE-Dateien können keine InProc-Server sein.                                                                                                                            |
| DIE CLSID "{GUID1}" im Kontext "InProcServer32" weist ein Argument auf. Nur LocalServer-Kontexte können Argumente aufweisen.                              | Entfernen Sie das -Argument, um diesen Fehler zu beheben.                                                                                                                                                                                   |
| CLSID "{GUID1}" im Kontext "InProcServer32" gibt einen InProc-Standardwert an. Nur LocalServer-Kontexte können Standardmäßige InProc-Werte aufweisen. | Es gibt ein Objekt mit einem InProc-Standardwert, bei dem es sich nicht um ein Objekt handelt, das in den Kontexten LocalServer oder LocalServer32 verwendet wird. Um diesen Fehler zu beheben, entfernen Sie den DeflnProc-Wert, oder ändern Sie den Kontext der -Klasse.<br/> |



 

[Klassentabelle](class-table.md) (partiell)



| CLSID   | Kontext        | Komponente\_ | DefInProcHandler | Argument |
|---------|----------------|-------------|------------------|----------|
| {GUID1} | Inprocserver32 | Component1  | InProcServer     | Arg      |



 

[Komponententabelle](component-table.md) (teilweise)



| Komponente  | KeyPath |
|------------|---------|
| Component1 | Datei1   |



 

[Dateitabelle](file-table.md) (partiell)



| Datei  | Dateiname |
|-------|----------|
| Datei1 | test.exe |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




