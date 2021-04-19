---
description: Die Klassen Tabelle enthält com-Server bezogene Informationen, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile kann einen Satz von Registrierungs Schlüsseln und-Werten generieren. Die zugehörigen ProgID-Informationen sind in dieser Tabelle enthalten.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Klassen Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348339"
---
# <a name="class-table"></a>Klassen Tabelle

Die Klassen Tabelle enthält com-Server bezogene Informationen, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile kann einen Satz von Registrierungs Schlüsseln und-Werten generieren. Die zugehörigen ProgID-Informationen sind in dieser Tabelle enthalten.

Die Klassen Tabelle weist die folgenden Spalten auf.



| Spalte           | Typ                         | Schlüssel | Nullwerte zulässig |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | J   | N        |
| Kontext          | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_      | [Bezeichner](identifier.md) | J   | N        |
| ProgID- \_ Standard  | [Text](text.md)             | N   | J        |
| BESCHREIBUNG      | [Text](text.md)             | N   | J        |
| AppId\_          | [GUID](guid.md)             | N   | J        |
| Filetypemask     | [Text](text.md)             | N   | J        |
| Symbol\_           | [Bezeichner](identifier.md) | N   | J        |
| IconIndex        | [Integer](integer.md)       | N   | J        |
| Definprochandler | [Filename](filename.md)     | N   | J        |
| Argument         | [Großformatige](formatted.md)   | N   | J        |
| Funktion\_        | [Bezeichner](identifier.md) | N   | N        |
| Attribute       | [Integer](integer.md)       | N   | J        |



 

## <a name="column-information"></a>Spalten Informationen

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

Der Klassen Bezeichner (ID) eines COM-Servers.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Kontext
</dt> <dd>

Der Server Kontext für diesen Server. Geben Sie einen der folgenden Werte für den CLSID-Schlüssel ein.



| CLSID-Schlüssel                             | BESCHREIBUNG                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.             |
| [LocalServer32](../com/localserver32.md)   | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.             |
| [InprocServer](../com/inprocserver.md)     | Gibt den Pfad zu einer Prozess internen Server-DLL an.                           |
| [InprocServer32](../com/inprocserver32.md) | Gibt den Pfad zu einem in-Process-32-Bit-Server und dem Threading Modell an. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in der [Komponenten Tabelle](component-table.md) , der die Komponente angibt, deren Schlüsseldatei den com-Server bereitstellt.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgID- \_ Standard
</dt> <dd>

Die standardmäßige Programm-ID, die dieser Klassen-ID zugeordnet ist. Diese Spalte ist ein Fremdschlüssel in der [ProgID-Tabelle](progid-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Lokalisierte Beschreibung, die der Klassen-ID und Programm-ID zugeordnet ist.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppID\_
</dt> <dd>

Anwendungs-ID mit DCOM-Informationen für die zugeordnete Anwendung (Zeichen folgen- [GUID](guid.md)). Diese Spalte ist ein Fremdschlüssel in die [AppID-Tabelle](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>Filetypemask
</dt> <dd>

Enthält Informationen für den Schlüssel HKCR (this CLSID).

Wenn mehrere Muster vorhanden sind, müssen Sie durch ein Semikolon getrennt werden, und es werden numerische Unterschlüssel generiert: 0, 1, 2... Weitere Informationen zu dieser Funktionalität finden Sie unter [**getclassfile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Angezeigt\_
</dt> <dd>

Die Datei, die das Symbol bereitstellt, das dieser CLSID zugeordnet ist. Das Installationsprogramm schreibt den Eintrag in dieser Spalte unter den der ProgID zugeordneten DefaultIcon-Schlüssel. Wenn er nicht NULL ist, ist die Spalte ein Fremdschlüssel in der [Symboltabelle](icon-table.md). Wenn er NULL ist, stellt der com-Server die Symbol Ressource bereit. Bei angekündigten Dateizuordnungen und Verknüpfungen ist in dieser Spalte ein Wert ungleich NULL erforderlich, um ordnungsgemäß angezeigt zu werden.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Symbol Index in der Symbol Datei. Diese kann NULL sein.

Nur nicht negative Zahlen.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>Definprochandler
</dt> <dd>

Dieses Feld gibt den in-Process-Standard Handler für den Server Kontext an, der im Kontext Feld angegeben ist.

Dieses Feld muss NULL sein, wenn ein InprocServer-oder InprocServer-CLSID-Schlüssel im Kontext Feld angezeigt wird.

Wenn ein LocalServer-oder LocalServer32 CLSID-Schlüssel im Kontext Feld angezeigt wird, identifiziert der Wert im Feld definprochandler den standardmäßigen Prozess internen Handler.



| Wert                | BESCHREIBUNG                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nicht numerischer Wert    | Das Installationsprogramm behandelt einen nicht numerischen Wert im Feld definprochandler als Systemdatei, die als 32-Bit-Prozess interne, in-Process-Handler, der durch den InprocHandler32-Schlüssel angegeben ist, fungiert.                                                                                                            |
| Null                 | Die Felder "definprochandler" und "Argument" können für einen LocalServer-oder LocalServer32 CLSID-Schlüssel NULL sein.                                                                                                                                                                           |
| 1 = Standard (System) | Der Standardwert ist der von InprocHandler angegebene 16-Bit-in-Process-Handler. In diesem Fall ist der Wert von InprocHandler der Name in der Registrierung, mit dem der Wert des in-Process-Standard Handlers gespeichert wird. Beispiel: HKEY- \_ \_ Software Klassen für lokale Computer \\ \\ \\ CLSID.     |
| 2 = Standard (System) | Der Standardwert ist der 32-Bit-in-Process-Handler, der durch InprocHandler32 angegeben wird. In diesem Fall ist der Wert von InprocHandler32 der Name in der Registrierung, mit dem der Wert des in-Process-Standard Handlers gespeichert wird. Beispiel: HKEY- \_ \_ Software Klassen für lokale Computer \\ \\ \\ CLSID. |
| 3 = Standard (System) | Der Standardwert ist ein in-Process-Handler mit 16-Bit-oder 32-Bit-Prozess.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten
</dt> <dd>

Wenn ein LocalServer-oder LocalServer32 CLSID-Schlüssel im Kontext Feld angezeigt wird, wird der Text in diesem Feld als Argument für den Server registriert und von com zum Aufrufen des Servers verwendet. Die Felder "definprochandler" und "Argument" können NULL sein, wenn "LocalServer" oder "localserver32" im Kontext Feld angezeigt wird.

Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argument eingeschränkt ist. Eine Eigenschaft, die als \[ Eigenschaft \] in diesem Feld formatiert ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits den vorgesehenen Wert aufweist, wenn die Komponente, die die Klasse besitzt, installiert ist. Damit das Argument "MyDoc.doc" z. b. \[ \# \] in den richtigen Wert aufgelöst wird, muss der gleiche Prozess die Datei MyDoc.doc und die Komponente installieren, die die Klasse besitzt.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel in der [Featuretabelle](feature-table.md) , der die Funktion angibt, die den com-Server bereitstellt.

Externer Schlüssel für Spalte einer der featuretabellen.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Wenn in dieser Spalte " **msidbClassAttributesRelativePath** " festgelegt ist, kann der Bare-Dateiname für com-Server verwendet werden. Der Dateiname wird nur von dem Installer anstelle des gesamten Pfads registriert. Dadurch kann der Server im aktuellen Verzeichnis Vorrang haben und mehrere Kopien derselben Komponente zulassen.



| Attribut                            | Decimal | Hexadezimal |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird beim Ausführen der [RegisterClassInfo-Aktion](registerclassinfo-action.md) oder der [unregisterclassinfo-Aktion](unregisterclassinfo-action.md) bezeichnet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE41](ice41.md)  
[ICE42](ice42.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
