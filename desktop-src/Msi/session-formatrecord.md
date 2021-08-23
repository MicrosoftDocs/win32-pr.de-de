---
description: Die FormatRecord-Methode des Session-Objekts gibt eine formatierte Zeichenfolge aus einer Vorlage zurück und zeichnet Daten auf.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session.FormatRecord-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f58aabc0bd222b22ee74cb0b431ce8051ed6bad546d963160c922bd86dee2383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629150"
---
# <a name="sessionformatrecord-method"></a>Session.FormatRecord-Methode

Die **FormatRecord-Methode** des [**Session-Objekts**](session-object.md) gibt eine formatierte Zeichenfolge aus einer Vorlage zurück und zeichnet Daten auf.

## <a name="syntax"></a>Syntax


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*record* 
</dt> <dd>

Erforderliches **Datensatzobjekt,** das eine Vorlage und daten enthält, die formatiert werden sollen. Die Vorlagenzeichenfolge muss in Feld 0 festgelegt werden, gefolgt von allen Datenparametern, auf die verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **FormatRecord-Methode** verwendet den folgenden Formatprozess.

Parameter, die [formatiert](formatted.md) werden sollen, werden in eckige Klammern \[ \] eingeschlossen. . Die eckigen Klammern können iteriert werden, da die Ersetzungen von innen nach außen aufgelöst werden.

Wenn ein Teil der Zeichenfolge in geschweifte Klammern { } eingeschlossen ist und keine eckigen Klammern enthält, bleibt der Teil unverändert, einschließlich der geschweiften Klammern.

Wenn ein Teil der Zeichenfolge in geschweifte Klammern eingeschlossen ist und einen oder mehrere Eigenschaftsnamen enthält und alle Eigenschaften gefunden werden, wird der Text (mit den aufgelösten Ersetzungen) ohne die geschweiften Klammern angezeigt. Wenn keine der Eigenschaften gefunden wird, werden der gesamte Text in den geschweiften Klammern und die geschweiften Klammern selbst entfernt.

**So formatieren Sie Zeichenfolgen mithilfe der FormatRecord-Methode**

1.  Die numerischen Parameter werden ersetzt, indem der Marker durch den Wert des entsprechenden Datensatzfelds ersetzt wird, wobei fehlende werte oder NULL-Werte keinen Text erzeugen.
2.  Die Ergebniszeichenfolge wird verarbeitet, indem die Nicht-Datensatzparameter durch die entsprechenden Werte ersetzt werden, wie in den folgenden Beschreibungen angegeben.
    -   Wenn eine Teilzeichenfolge der Form \[ "Eigenschaftsname" \] gefunden wird, wird sie durch den Wert der -Eigenschaft ersetzt.
    -   Wenn eine Teilzeichenfolge im Format \[ "%environmentvariable" \] gefunden wird, wird der Wert der Umgebungsvariablen ersetzt.
    -   Wenn eine Teilzeichenfolge des \[ \# *Formdateischlüssels* \] gefunden wird, wird sie durch den vollständigen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in der [Dateitabelle](file-table.md)verwendet wird. Der Wert von \[ \# *filekey* \] bleibt leer und wird erst durch einen Pfad ersetzt, wenn das Installationsprogramm die Aktion [CostInitialize,](costinitialize-action.md)die [FileCost-Aktion](filecost-action.md)und die [CostFinalize-Aktion](costfinalize-action.md)ausführt. Der Wert von \[ \# *filekey* \] hängt vom Installationsstatus der Komponente ab, zu der die Datei gehört. Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert der Pfad zum Quellspeicherort der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert der Pfad zum Zielspeicherort der Datei nach der Installation. Wenn die Komponente nicht vorhanden ist, ist der Pfad leer. Weitere Informationen zum Überprüfen des Installationsstatus von Komponenten finden Sie unter [Überprüfen der Installation von Features, Komponenten und Dateien.](checking-the-installation-of-features-components-files.md)
    -   Wenn eine Teilzeichenfolge des Formulars \[ *$componentkey* \] gefunden wird, wird sie durch das Installationsverzeichnis der Komponente durch den Wert *componentkey* ersetzt, der als Schlüssel in der [Tabelle Komponente](component-table.md)verwendet wird. Der Wert von \[ $ *componentkey* \] bleibt leer und wird erst durch ein Verzeichnis ersetzt, wenn das Installationsprogramm die Aktion [CostInitialize,](costinitialize-action.md)die [FileCost-Aktion](filecost-action.md)und die [CostFinalize-Aktion](costfinalize-action.md)ausführt. Der Wert von \[ $ *componentkey* \] hängt vom Installationsstatus der Komponente ab. Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert das Quellverzeichnis der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert nach der Installation das Zielverzeichnis. Wenn die Komponente nicht vorhanden ist, wird der Wert leer gelassen. Weitere Informationen zum Überprüfen des Installationsstatus von Komponenten finden Sie unter [Überprüfen der Installation von Features, Komponenten und Dateien.](checking-the-installation-of-features-components-files.md)
    -   Wenn eine Teilzeichenfolge im Format \[ \\ \] "c" gefunden wird, wird sie ohne weitere Verarbeitung durch das Zeichen ersetzt. Nur das erste Zeichen nach dem umgekehrten Schrägstrich wird beibehalten. alles andere wird entfernt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Formatiert](formatted.md)
</dt> <dt>

[Spaltendatentypen](column-data-types.md)
</dt> </dl>

 

 




