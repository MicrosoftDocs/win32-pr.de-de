---
description: Ein externer Benutzeroberflächen Handler kann die Liste der vom dwmessagedfilter-Parameter der msisettexternalui-Funktion angegebenen Installationsprogramm Nachrichten verarbeiten.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Windows Installer Meldungen werden verarbeitet.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215360"
---
# <a name="parsing-windows-installer-messages"></a>Windows Installer Meldungen werden verarbeitet.

Ein externer Benutzeroberflächen Handler kann die Liste der vom *dwmessagedfilter* -Parameter der [**msisettexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) -Funktion angegebenen Installationsprogramm Nachrichten verarbeiten. Einige dieser Nachrichten enthalten Zeichen folgen, die direkt verwendet werden können. andere Meldungen müssen möglicherweise analysiert und vom externen UI-Handler verarbeitet werden, damit Sie hilfreich sind. Der externe Benutzeroberflächen Handler muss möglicherweise nur Windows Installer Nachrichten überwachen, ohne einen Vorgang auszuführen, der sich auf die Installation auswirkt.

Die folgenden Windows Installer Meldungen enthalten Zeichen folgen, die von einem Dialogfeld angezeigt werden können und keine zusätzliche Verarbeitung erfordern. Diese Meldungen enthalten eine Liste von Schaltflächen und Symbolen, die von einem Dialogfeld angezeigt werden sollen. Zum Angeben von Symbolen und Schaltflächen können Sie die Werte für die **\_ typemasken** "MB", "MB" und **"MB" \_** verwenden. **\_**

<dl> <dt>

<span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**installmessage \_ fatalexit**
</dt> <dd>

Eine vorzeitige Beendigung der Installation ist aufgetreten.

</dd> <dt>

<span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**installmessage- \_ Fehler**
</dt> <dd>

Formatierte Fehlermeldung.

</dd> <dt>

<span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**installmessage- \_ Warnung**
</dt> <dd>

Formatierte Warnmeldung.

</dd> <dt>

<span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**installmessage- \_ Info**
</dt> <dd>

Formatierte Protokollmeldung.

</dd> <dt>

<span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**installmessage- \_ Benutzer**
</dt> <dd>

Formatierte Benutzer Meldung.

</dd> <dt>

<span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**installmessage \_ oudeatdiskspace**
</dt> <dd>

Formatierte Meldung, die auf eine nicht genügend Speicherplatz Bedingung hinweist

</dd> </dl>

Der externe Benutzer Handler kann die folgenden Windows Installer Nachrichten verwenden, um eine Sequenz der Windows Installer-Benutzeroberfläche zu überwachen. Das Installationsprogramm sendet diese Nachrichten zu Beginn einer Windows Installer UI-Sequenz, wenn jedes Dialogfeld angezeigt wird, und am Ende der UI-Sequenz. Es ist keine Verarbeitung erforderlich, um diese Nachrichten zu verwenden.

<dl> <dt>

<span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>installmessage \_ Beenden
</dt> <dd>

Diese Meldung gibt das Ende der UI-Sequenz an. Die Zeichenfolge ist eine NULL-Zeichenfolge.

</dd> <dt>

<span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>installmessage \_ initialisieren
</dt> <dd>

Diese Meldung gibt an, dass die UI-Sequenz gestartet wurde. Die Zeichenfolge ist eine NULL-Zeichenfolge.

</dd> <dt>

<span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>installmessage \_ Show Dialog
</dt> <dd>

Die Zeichenfolge enthält den Namen des aktuellen Dialog Felds.

</dd> </dl>

Die folgenden Windows Installer Meldungen erfordern eine zusätzliche Verarbeitung durch den externen UI-Handler.

<dl> <dt>

<span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**installmessage \_ ResolveSource**
</dt> <dd>

Der externe Benutzeroberflächen Handler muss 0 (null) zurückgeben und es Windows Installer ermöglichen, die Nachricht zu verarbeiten. Der Handler für die externe Benutzeroberfläche kann diese Meldung überwachen, sollte jedoch keine Aktionen ausführen, die sich auf die Installation auswirken.

</dd> <dt>

<span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**installmessage \_ FilesInUse**
</dt> <dd>

Die externe Benutzeroberfläche sollte in Reaktion auf diese Meldung ein [FilesInUse-Dialog](filesinuse-dialog.md) Feld anzeigen.

</dd> <dt>

<span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**installmessage \_ rmfilesinuse**
</dt> <dd>

Die externe Benutzeroberfläche sollte in Reaktion auf diese Meldung ein [msirmfilesinuse-Dialog](msirmfilesinuse-dialog.md) Feld anzeigen. Verfügbar ab Windows Installer Version 4,0. Weitere Informationen zu dieser Meldung finden [Sie unter Verwenden des Neustart-Managers mit einer externen Benutzeroberfläche](using-restart-manager-with-an-external-ui-.md).

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**installmessage- \_ Aktions Start**
</dt> <dd>

Diese Meldung enthält Informationen über die aktuelle Aktion. Das Format ist Aktion \[ 1 \] : \[ 2 \] . \[3 \] , wobei ein Doppelpunkt verwendet wird, um Feld 1 und Feld 2 zu trennen, und ein Punkt zum Trennen von Feld 2 und Feld 3 verwendet wird. Feld \[ 1 \] enthält den Zeitpunkt, zu dem die Aktion mit dem [**Zeit**](time.md) Eigenschaften Format gestartet wurde. Feld \[ 2 \] enthält den Namen der Aktion aus der Sequenz Tabelle. Field \[ 3 \] gibt die Beschreibung der Aktion aus der [Action Text-Tabelle](actiontext-table.md) oder aus der [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion.

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**installmessage- \_ Aktions Daten**
</dt> <dd>

Das Format dieser Zeichenfolge wird durch den [Vorlagen](template.md) Wert angegeben, der in der [Tabelle "aktiontext](actiontext-table.md) " oder der Funktion " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " bereitgestellt wird. Nach der Meldung " **installmessage- \_ Aktions Start** " kann eine unbegrenzte Anzahl von **installmessage- \_ Aktions Daten** Nachrichten vorhanden sein.

</dd> <dt>

<span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**installmessage \_ commondata**
</dt> <dd>

Diese Meldung enthält drei Untertypen: Sprache, Beschriftung und cancelshow. Die Zeichenfolge kann drei Felder enthalten, die durch eine Zahl gefolgt von einem Doppelpunkt getrennt sind. Es sind nicht alle Felder erforderlich. Die Nachricht kann eine NULL-oder leere Zeichenfolge ("") sein.

<dl> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse
</dt> <dd>

Feld 1 enthält den Wert 0, um anzugeben, dass diese Zeichenfolge Sprachinformationen enthält. Feld 2 enthält einen [sprach](language.md) Wert, bei dem es sich um einen numerischen sprach Bezeichner (langid) handelt. Field 3 ist ein Wert, der eine ANSI-Codepage darstellt.

</dd> <dt>

<span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Unter
</dt> <dd>

Feld 1 enthält den Wert 1, um anzugeben, dass diese Zeichenfolge den Text einer Beschriftung oder eines Titels enthält. Feld 2 enthält Text, der von einem externen Benutzeroberflächen Handler als Titel Titel für ein Dialogfeld verwendet werden kann. Field 3 ist NULL oder eine leere Zeichenfolge (""). Feld 3 kann nicht in der Beschriftungs Nachricht vorhanden sein.

</dd> <dt>

<span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>Abbrechen
</dt> <dd>

Feld 1 enthält den Wert 2, um anzugeben, dass diese Zeichenfolge Informationen darüber enthält, ob die Schaltfläche Abbrechen angezeigt werden soll. Wenn die Schaltfläche Abbrechen ausgeblendet werden soll, enthält Feld 2 den Wert 0. Wenn die Schaltfläche Abbrechen sichtbar sein soll, enthält Feld 2 den Wert 1.

</dd> </dl> </dd> <dt>

<span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>installmessage \_ -Status
</dt> <dd>

Diese Nachricht hat vier Untertypen: Reset, AktionInfo, progressreport und progressaddition. Der externe Handler sollte erst dann auf eine dieser Nachrichten reagieren, wenn die erste Statusmeldung zum Zurücksetzen empfangen wird. Dadurch wird eine Schätzung der Gesamtzahl der Ticks für die Statusanzeige bereitstellt.

<dl> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Festlegen
</dt> <dd>

Feld 1 enthält den Wert 0, um das Zurücksetzen der Statusanzeige anzugeben. Feld 2 enthält die Gesamtanzahl der Ticks in der Statusanzeige. Field 3 enthält den Wert 0 für die Bewegung der vorwärts Statusanzeige. Field 3 enthält den Wert 1 für die Bewegung der rückwärts Statusanzeige. Der Wert 0 in Feld 4 bedeutet, dass die Installation ausgeführt wird und die verbleibende Zeit berechnet werden kann. Der Wert 1 in Feld 4 bedeutet, dass das Skript ausgeführt wird und ein "Bitte warten..." die Meldung kann angezeigt werden. Der Schätzwert für die Gesamtzahl der Ticks ist eine Näherung und möglicherweise ungenau.

</dd> <dt>

<span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>Action Info
</dt> <dd>

Feld 1 enthält den Wert 1, um anzugeben, dass diese Zeichenfolge Aktions Informationen enthält. Feld 2 enthält die Anzahl der Ticks, die die Statusanzeige für jede von der aktuellen Aktion gesendete Action Data-Nachricht verschiebt. Wenn Feld 3 den Wert 0 (null) enthält, ignorieren Sie Feld 2. Wenn Feld 3 den Wert 1 enthält, erhöhen Sie die Statusanzeige um die Anzahl der Ticks in Feld 2 für jede von der aktuellen Aktion gesendete Aktion "action Data". Field 4 wird nicht verwendet.

</dd> <dt>

<span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>Progressreport
</dt> <dd>

Feld 1 enthält den Wert 2, um anzugeben, dass diese Zeichenfolge Statusinformationen enthält. Feld 2 enthält die Anzahl der Ticks, die die Statusanzeige verschoben hat. Feld 3 wird nicht verwendet. Field 4 wird nicht verwendet.

</dd> <dt>

<span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>Progressaddition
</dt> <dd>

Feld 1 enthält den Wert 3, um anzugeben, dass eine Aktion Ticks die Statusanzeige hinzufügen kann. Feld 2 enthält die Anzahl der Ticks, die der Gesamtanzahl der erwarteten Anzahl von Status Ticks hinzugefügt werden sollen. Feld 3 wird nicht verwendet. Field 4 wird nicht verwendet.

</dd> </dl> </dd> </dl>

 

 



