---
description: 'Wsdcodegen verfügt über zwei Funktionen: das Erstellen von Konfigurationsdateien und das Erstellen von Quellcode für WSDAPI-Client-und-Host Anwendungen.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Wsdcodegen-Befehlszeilen Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863751"
---
# <a name="wsdcodegen-command-line-syntax"></a>Wsdcodegen-Befehlszeilen Syntax

Wsdcodegen verfügt über zwei Funktionen: das Erstellen von Konfigurationsdateien und das Erstellen von Quellcode für WSDAPI-Client-und-Host Anwendungen. Dieses Thema enthält die Befehlszeilen Syntax, die zum Ausführen der einzelnen Aufgaben verwendet wird.

## <a name="generating-a-configuration-file"></a>Erstellen einer Konfigurationsdatei

### <a name="syntax"></a>Syntax

**WSDCODEGEN.EXE** **/generateconfig:**{**Client** \| **Host** \| **all**} **\[ /OutputFile:**_configfilename_ *_\]_* *wsdlfilename amelist*

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: {Client \| Host \| alle}**
</dt> <dd>

Der Codetyp, der von der Ausgabe Konfigurationsdatei generiert wird. **/generateconfig: Client** wird verwendet, um eine Konfigurationsdatei zum Generieren von Client Code zu generieren, **/generateconfig: der Host** wird zum Generieren einer Konfigurationsdatei zum Generieren des Host Codes verwendet, und **/generateconfig: all** wird verwendet, um eine Konfigurationsdatei zum Generieren von Client-und Hostcode zu generieren.

</dd> <dt>

<span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/OutputFile:**_configfilename_
</dt> <dd>

Dieser optionale Parameter wird verwendet, um den Dateinamen der Ausgabe Konfigurationsdatei anzugeben. Wenn dieser Parameter ausgeschlossen wird, wird der Name der Ausgabe Konfigurationsdatei codegen.config.

</dd> <dt>

<span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*
</dt> <dd>

Fügen Sie eine PnP-X-Vorlage in die Konfigurationsdatei ein.

</dd> <dt>

<span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*Wsdldatamelist*
</dt> <dd>

Eine durch Leerzeichen getrennte Liste der WSDL-Dateien, die von wsdcodegen verarbeitet werden sollen.

</dd> </dl>

## <a name="generating-source-code"></a>Quellcode wird erzeugt

### <a name="syntax"></a>Syntax

**WSDCODEGEN.EXE** **/GenerateCode** **\[ /Download \]** **\[ /GBC \]** **\[ outputroot:**_path_ *_\]_* **\[ /writeaccess:**_Befehl_ *_\]_* *configfilename*

### <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**
</dt> <dd>

Weist wsdcodegen an, Quellcode zu generieren. Dies ist der Standardmodus, wenn kein Modus angegeben wird.

</dd> <dt>

<span id="_download"></span><span id="_DOWNLOAD"></span>**/Download**
</dt> <dd>

Herunterladen importierter Dokumente, auf die von der Konfigurationsdatei verwiesen wird Dieser Parameter ist optional.

</dd> <dt>

<span id="_gbc"></span><span id="_GBC"></span>**/gbc**
</dt> <dd>

Fügt dem Quellcode Kommentare hinzu, die angeben, dass der Code generiert wurde. Diesen Kommentaren wird der Ausdruck "generiert von" vorangestellt. Dieser Parameter ist optional.

</dd> <dt>

<span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_Pfad_
</dt> <dd>

Der Ausgabe Speicherort für generierte Dateien. der *Pfad* kann ein absoluter oder relativer Pfad sein. Dieser Parameter ist optional.

</dd> <dt>

<span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_Befehl_
</dt> <dd>

Weist wsdcodegen an, den angegebenen Befehl auszuführen, bevor vorhandene Dateien auf dem Datenträger geändert werden. Ausgabedateien, die mit den Daten auf dem Datenträger identisch sind, erhalten diesen Befehl nicht, und Sie werden auch nicht in geschrieben. Wenn der Befehl die Sequenz " {0} " enthält, wird diese Sequenz durch den Dateinamen der Datei ersetzt, die geändert werden soll. Wenn dies nicht der Fall ist, wird der Dateiname an den Befehl angehängt.

Beispiele:

**/writeaccess: "atungb-r"**

**/writeaccess: "atungb-r {0} "**

**/writeaccess: "kopieren {0} .. \\ Sichern \\ "**

</dd> <dt>

<span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Configfilename*
</dt> <dd>

Der Name der Konfigurationsdatei, die vor dem Erstellen von Code verarbeitet werden soll.

</dd> </dl>

## <a name="formatting-legend"></a>Formatierungslegende



| Format                                                                    | Bedeutung                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| *Kursiv*                                                                  | Informationen, die der Benutzer bereitstellen muss                  |
| **Fett**                                                                  | Elemente, die der Benutzer genau so eingeben muss, wie sie angezeigt werden       |
| Zwischen eckigen Klammern ( \[ \] )                                                   | Optionale Elemente                                          |
| Zwischen geschweiften Klammern ( {} ); durch Pipe getrennte Optionen ( \| ). Beispiel: {Even \| Odd} | Satz von Auswahlmöglichkeiten, von denen der Benutzer nur eine auswählen muss |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wsdcodegen-Konfigurationsdatei](wsdcodegen-configuration-file.md)
</dt> <dt>

[Verwenden von wsdcodegen](using-wsdcodegen.md)
</dt> </dl>

 

 




