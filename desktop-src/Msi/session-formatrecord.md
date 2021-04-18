---
description: Die formatrecord-Methode des Session-Objekts gibt eine formatierte Zeichenfolge aus einer Vorlage und Daten Satz Daten zurück.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Session. formatrecord-Methode
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
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368517"
---
# <a name="sessionformatrecord-method"></a>Session. formatrecord-Methode

Die **formatrecord** -Methode des [**Session**](session-object.md) -Objekts gibt eine formatierte Zeichenfolge aus einer Vorlage und Daten Satz Daten zurück.

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

Erforderliches Daten **Satz** Objekt, das eine Vorlage und die zu formatierenden Daten enthält. Die Vorlagen Zeichenfolge muss in Feld 0, gefolgt von allen referenzierten Daten Parametern, festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **formatrecord** -Methode verwendet den folgenden Format Prozess.

Die zu [formatierenden](formatted.md) Parameter werden in eckige Klammern eingeschlossen \[ .. \] . Die eckigen Klammern können iteriert werden, da die Ersetzungen von innen nach oben aufgelöst werden.

Wenn ein Teil der Zeichenfolge in geschweiften Klammern ({}) eingeschlossen ist und keine eckigen Klammern enthält, bleibt der Teil unverändert, einschließlich der geschweiften Klammern.

Wenn ein Teil der Zeichenfolge in geschweiften Klammern eingeschlossen ist und einen oder mehrere Eigenschaftsnamen enthält, und wenn alle Eigenschaften gefunden werden, wird der Text (mit den aufgelösten Ersetzungen) ohne geschweifte Klammern angezeigt. Wenn eine der Eigenschaften nicht gefunden wird, werden der gesamte Text in den geschweiften Klammern und die geschweiften Klammern selbst entfernt.

**So formatieren Sie Zeichen folgen mithilfe der formatrecord-Methode**

1.  Die numerischen Parameter werden ersetzt, indem der Marker durch den Wert des entsprechenden Daten Satz Felds ersetzt wird, wobei fehlende oder NULL-Werte keinen Text erzeugen.
2.  Die Zeichenfolge, die sich ergibt, wird verarbeitet, indem die nicht-Datensatz-Parameter durch die entsprechenden Werte ersetzt werden, wie in den folgenden Beschreibungen angegeben.
    -   Wenn eine Teil Zeichenfolge der Form " \[ propertyName" gefunden wird \] , wird Sie durch den Wert der-Eigenschaft ersetzt.
    -   Wenn eine Teil Zeichenfolge der Form " \[ % Umgebungsvariable \] " gefunden wird, wird der Wert der Umgebungsvariablen ersetzt.
    -   Wenn eine Teil Zeichenfolge der Form \[ \# *filekey* \] gefunden wird, wird Sie durch den vollständigen Pfad der Datei ersetzt, wobei der Wert *filekey* als Schlüssel in die [Dateitabelle](file-table.md)verwendet wird. Der Wert von \[ \# *filekey* \] bleibt leer und wird nicht durch einen Pfad ersetzt, bis der Installer die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführt. Der Wert von \[ \# *filekey* \] hängt vom Installationsstatus der Komponente ab, zu der die Datei gehört. Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert der Pfad zum Quell Speicherort der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert der Pfad zum Zielort der Datei nach der Installation. Wenn die Komponente nicht vorhanden ist, ist der Pfad leer. Weitere Informationen zum Überprüfen des Installationsstatus von-Komponenten finden Sie unter über [Prüfen der Installation von Features, Komponenten und Dateien](checking-the-installation-of-features-components-files.md).
    -   Wenn eine Teil Zeichenfolge der Form \[ *$componentkey* \] gefunden wird, wird Sie durch das Installationsverzeichnis der Komponente ersetzt, wobei der Wert *componentkey* als Schlüssel in der [Komponenten Tabelle](component-table.md)verwendet wird. Der Wert von \[ $ *componentkey* \] bleibt leer und wird erst durch ein Verzeichnis ersetzt, wenn das Installationsprogramm die Aktion " [costinitialize](costinitialize-action.md)", " [filecost Action](filecost-action.md)" und " [costfinalize](costfinalize-action.md)" ausführt. Der Wert von \[ $ *componentkey* \] hängt vom Installationsstatus der Komponente ab. Wenn die Komponente aus der Quelle ausgeführt wird, ist der Wert das Quellverzeichnis der Datei. Wenn die Komponente lokal ausgeführt wird, ist der Wert das Zielverzeichnis nach der Installation. Wenn die Komponente nicht vorhanden ist, wird der Wert leer gelassen. Weitere Informationen zum Überprüfen des Installationsstatus von-Komponenten finden Sie unter über [Prüfen der Installation von Features, Komponenten und Dateien](checking-the-installation-of-features-components-files.md).
    -   Wenn eine Teil Zeichenfolge der Form " \[ \\ c \] " gefunden wird, wird Sie ohne weitere Verarbeitung durch das Zeichen ersetzt. Nur das erste Zeichen nach dem umgekehrten Schrägstrich wird beibehalten. alles andere wird entfernt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Großformatige](formatted.md)
</dt> <dt>

[Spaltendatentypen](column-data-types.md)
</dt> </dl>

 

 




