---
description: Windows Installer Entwickler können das Installationspaket für den Neustart-Manager vorbereiten, indem Sie die unter Verwenden von Windows Installer mit dem Neustart-Manager beschriebenen Richtlinien befolgen.
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: Verwenden des Neustart-Managers mit einer externen Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f112884669b173b40f3806c48cf8e05308c5b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214628"
---
# <a name="using-restart-manager-with-an-external-ui"></a>Verwenden des Neustart-Managers mit einer externen Benutzeroberfläche

Windows Installer Entwickler können das Installationspaket für den Neustart- [Manager](../rstmgr/restart-manager-portal.md) vorbereiten, indem Sie die unter [Verwenden von Windows Installer mit dem Neustart-Manager](using-windows-installer-with-restart-manager.md)beschriebenen Richtlinien befolgen.

Geben Sie den "installlogmode"- \_ Meldungstyp "rmfilesinuse" an, wenn Sie die [**msisettexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) -oder [**msisettexternaluirecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) -Funktion aufrufen, um den externen Benutzeroberflächen Handler zu aktivieren Windows Installer sendet dann eine installmessage \_ -rmfilesinuse-Nachricht zur Verwendung durch externe Benutzeroberflächen Handler, die den [Neustart-Manager](../rstmgr/restart-manager-portal.md)unterstützen.

Der externe Benutzeroberflächen Handler sollte die Informationen verarbeiten, die in installmessage- \_ rmfilesinuse-Meldungen enthalten sind. Wenn keine registrierte oder interne Benutzeroberfläche die installmessage- \_ rmfilesinuse-Nachricht behandelt, sendet Windows Installer eine installmessage \_ FilesInUse-Nachricht zur Verwendung durch vorhandene externe Handler, die installmessage \_ FilesInUse-Meldungen und das [FilesInUse](filesinuse-dialog.md) -Dialogfeld unterstützen.

Die externe Benutzeroberfläche kann die in der folgenden Tabelle aufgeführten Werte zurückgeben.



| Rückgabewert der externen Benutzeroberfläche | Von Windows Installer ausgeführte Aktion                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | Der Benutzer hat die Schaltfläche **OK** gedrückt. Der Windows Installer fordert an, dass der [Neustart-Manager](../rstmgr/restart-manager-portal.md) die Anwendungen, die derzeit verwendete Dateien enthalten, heruntergefahren und neu gestartet werden.                                                                                                                                               |
| IDCANCEL                 | Die Schaltfläche **Abbrechen** wurde gedrückt. Brechen Sie die Installation ab.                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | Die **ignorieren** -Schaltfläche wurde gedrückt. Die Installation wird ignoriert und fortgesetzt. Am Ende der Installation ist ein Neustart erforderlich.                                                                                                                                                                                                            |
| IDNO                     | Die Schaltfläche **Nein** wurde gedrückt. Wenn das Paket über ein [msirmfilesinuse](msirmfilesinuse-dialog.md) -Dialogfeld verfügt, senden Sie eine 1610-Nachricht. Weitere Informationen finden Sie unter [Windows Installer Fehlermeldungen](windows-installer-error-messages.md). Wenn das Paket nicht über das Dialogfeld msirmfilesinuse verfügt, senden Sie eine installmessage \_ FilesInUse-Nachricht. |
| IDRETRY                  | Die **Wiederholungs** Schaltfläche wurde gedrückt. Senden Sie die Nachricht installmessage \_ FilesInUse.                                                                                                                                                                                                                                                                 |
| -1                       | Ein Fehler. Beenden Sie die Installation.                                                                                                                                                                                                                                                                                                                |



 

 

 
