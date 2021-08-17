---
description: Die Tabelle Class enthält com serverbezogene Informationen, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile kann einen Satz von Registrierungsschlüsseln und -werten generieren. Die zugeordneten ProgId-Informationen sind in dieser Tabelle enthalten.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Klassentabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48985bd2d7e9670c89df53993e7170dc3e0e43a2b6e60f63d29e9f43e8d2ab3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066040"
---
# <a name="class-table"></a>Klassentabelle

Die Tabelle Class enthält com serverbezogene Informationen, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile kann einen Satz von Registrierungsschlüsseln und -werten generieren. Die zugeordneten ProgId-Informationen sind in dieser Tabelle enthalten.

Die Tabelle Class enthält die folgenden Spalten.



| Spalte           | Typ                         | Key | Nullwerte zulässig |
|------------------|------------------------------|-----|----------|
| CLSID            | [GUID](guid.md)             | J   | N        |
| Kontext          | [Identifier](identifier.md) | J   | N        |
| Komponente\_      | [Identifier](identifier.md) | J   | N        |
| \_ProgId-Standard  | [Text](text.md)             | N   | J        |
| BESCHREIBUNG      | [Text](text.md)             | N   | J        |
| Appid\_          | [GUID](guid.md)             | N   | J        |
| FileTypeMask     | [Text](text.md)             | N   | J        |
| Symbol\_           | [Identifier](identifier.md) | N   | J        |
| IconIndex        | [Integer](integer.md)       | N   | J        |
| DefInprocHandler | [Filename](filename.md)     | N   | J        |
| Argument         | [Formatiert](formatted.md)   | N   | J        |
| Komponente\_        | [Identifier](identifier.md) | N   | N        |
| Attribute       | [Integer](integer.md)       | N   | J        |



 

## <a name="column-information"></a>Spalteninformationen

<dl> <dt>

<span id="CLSID"></span><span id="clsid"></span>Clsid
</dt> <dd>

Der Klassenbezeichner (ID) eines COM-Servers.

</dd> <dt>

<span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Kontext
</dt> <dd>

Der Serverkontext für diesen Server. Geben Sie einen der folgenden Werte für den CLSID-Schlüssel ein.



| CLSID-SCHLÜSSEL                             | Beschreibung                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [LocalServer](../com/localserver.md)       | Gibt den vollständigen Pfad zu einer lokalen 16-Bit-Serveranwendung an.             |
| [LocalServer32](../com/localserver32.md)   | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.             |
| [InprocServer](../com/inprocserver.md)     | Gibt den Pfad zu einer Prozessserver-DLL an.                           |
| [Inprocserver32](../com/inprocserver32.md) | Gibt den Pfad zu einem 32-Bit-Prozessserver und dem Threadingmodell an. |



 

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der [Tabelle Komponente,](component-table.md) der die Komponente angibt, deren Schlüsseldatei den COM-Server bereitstellt.

</dd> <dt>

<span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>\_ProgId-Standard
</dt> <dd>

Die dieser Klassen-ID zugeordnete Standardprogramm-ID. Diese Spalte ist ein Fremdschlüssel in der [ProgID-Tabelle.](progid-table.md)

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Lokalisierte Beschreibung, die der Klassen-ID und Programm-ID zugeordnet ist.

</dd> <dt>

<span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>Appid\_
</dt> <dd>

Anwendungs-ID mit DCOM-Informationen für die zugeordnete Anwendung [(Zeichenfolgen-GUID).](guid.md) Diese Spalte ist ein Fremdschlüssel in der [AppId-Tabelle](appid-table.md).

</dd> <dt>

<span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask
</dt> <dd>

Enthält Informationen für den HKCR-Schlüssel (diese CLSID).

Wenn mehrere Muster vorhanden sind, müssen sie durch ein Semikolon getrennt werden, und numerische Unterschlüssel werden generiert: 0, 1, 2... Weitere Informationen zu dieser Funktionalität finden Sie unter [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Symbol\_
</dt> <dd>

Die Datei, die das symbol bereitstellt, das dieser CLSID zugeordnet ist. Das Installationsprogramm schreibt den Eintrag in dieser Spalte unter dem DefaultIcon-Schlüssel, der der ProgId zugeordnet ist. Wenn sie nicht NULL ist, ist die Spalte ein Fremdschlüssel in der [Symboltabelle](icon-table.md). Wenn er NULL ist, stellt der COM-Server die Symbolressource bereit. Angekündigte Dateizuordnungen und Verknüpfungen erfordern einen Wert ungleich NULL in dieser Spalte, um ordnungsgemäß angezeigt zu werden.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Symbolindex in die Symboldatei. Diese kann NULL sein.

Nur nicht negative Zahlen.

</dd> <dt>

<span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler
</dt> <dd>

Dieses Feld gibt den standardmäßigen In-Process-Handler für den im Feld Kontext angegebenen Serverkontext an.

Dieses Feld muss NULL sein, wenn ein InprocServer- oder InprocServer CLSID-Schlüssel im Feld Context angezeigt wird.

Wenn im Feld Context ein LocalServer- oder LocalServer32 CLSID-Schlüssel angezeigt wird, identifiziert der Wert im DefInprocHandler-Feld den standardmäßigen In-Process-Handler.



| Wert                | Beschreibung                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nicht numerischer Wert    | Das Installationsprogramm behandelt einen nicht numerischen Wert im DefInprocHandler-Feld als Systemdatei, die als 32-Bit-In-Process-Handler fungiert, der durch den InprocHandler32-Schlüssel angegeben wird.                                                                                                            |
| Null                 | Die Felder DefInprocHandler und Argument können für einen LocalServer- oder LocalServer32 CLSID-Schlüssel NULL sein.                                                                                                                                                                           |
| 1 = Standard (System) | Der Standardwert ist der von InprocHandler angegebene 16-Bit-In-Process-Handler. In diesem Fall ist der Wert von InprocHandler der Name in der Registrierung, unter der der Wert des Standardmäßigen In-Process-Handlers gespeichert wird. Beispiel: HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID.     |
| 2 = Standard (System) | Der Standardwert ist der 32-Bit-In-Process-Handler, der von InprocHandler32 angegeben wird. In diesem Fall ist der Wert von InprocHandler32 der Name in der Registrierung, unter der der Wert des standardmäßigen In-Process-Handlers gespeichert wird. Beispiel: HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID. |
| 3 = Standard (System) | Der Standardwert ist ein 16-Bit- oder 32-Bit-In-Process-Handler.                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Wenn im Feld Context ein LocalServer- oder LocalServer32 CLSID-Schlüssel angezeigt wird, wird der Text in diesem Feld als Argument für den Server registriert und von COM zum Aufrufen des Servers verwendet. Die Felder DefInprocHandler und Argument können beide NULL sein, wenn LocalServer oder LocalServer32 im Feld Kontext angezeigt wird.

Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argument eingeschränkt ist. Eine Eigenschaft, die in diesem Feld als Eigenschaft formatiert \[ \] ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits über den beabsichtigten Wert verfügt, wenn die Komponente installiert wird, die die Klasse besitzt. Wenn beispielsweise das Argument "MyDoc.doc" in \[ \# \] den richtigen Wert aufgelöst werden soll, muss derselbe Prozess die Datei MyDoc.doc und die Komponente installieren, die die Klasse besitzt.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Externer Schlüssel in der [Tabelle Feature,](feature-table.md) der das Feature angibt, das den COM-Server bereitstellt.

Externer Schlüssel, um eine der Featuretabellen zu spalten.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Wenn **msidbClassAttributesRelativePath** in dieser Spalte festgelegt ist, kann der reine Dateiname für COM-Server verwendet werden. Das Installationsprogramm registriert den Dateinamen nur anstelle des vollständigen Pfads. Dadurch hat der Server im aktuellen Verzeichnis Vorrang und lässt mehrere Kopien derselben Komponente zu.



| attribute                            | Decimal | Hexadezimal |
|--------------------------------------|---------|-------------|
| **msidbClassAttributesRelativePath** | 1       | 0x001       |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [RegisterClassInfo-Aktion](registerclassinfo-action.md) oder die [UnregisterClassInfo-Aktion](unregisterclassinfo-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfung

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

 

 
