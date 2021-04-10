---
description: In diesem Abschnitt wird beschrieben, wie Nachrichten von benutzerdefinierten Aktionen gesendet werden, die einen Teil der Installation durch Aufrufen einer Dynamic Link Library oder eines Skripts ausführen.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Zurückgeben von Fehlermeldungen von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480a9e7891680aadc9d8eb4eedba2bad0d2e3dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130669"
---
# <a name="returning-error-messages-from-custom-actions"></a>Zurückgeben von Fehlermeldungen von benutzerdefinierten Aktionen

In diesem Abschnitt wird beschrieben, wie Nachrichten von benutzerdefinierten Aktionen gesendet werden, die einen Teil der Installation durch Aufrufen einer Dynamic Link Library oder eines Skripts ausführen. Beachten Sie, dass der [benutzerdefinierte Aktionstyp 19](custom-action-type-19.md) nur eine angegebene Fehlermeldung sendet, einen Fehler zurückgibt und dann die Installation beendet. Der benutzerdefinierte Aktionstyp 19 führt keinen Teil der Installation aus.

Um eine Fehlermeldung von einer benutzerdefinierten Aktion zu senden, die eine [Dynamic Link Library](dynamic-link-libraries.md) (dll) verwendet, müssen Sie die benutzerdefinierte Aktion [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)abrufen. Beachten Sie, dass benutzerdefinierte Aktionen, die von einem [doaction ControlEvent](doaction-controlevent.md) gestartet werden, Nachrichten mit der [**Nachrichten**](session-message.md) Methode senden können, aber keine Nachricht mit **msiprocessmessage** senden können. Auf Systemen vor Windows Server 2003 können benutzerdefinierte Aktionen, die von einem doaction ControlEvent gestartet werden, keine Nachrichten mit der **msiprocessmessage** oder der **Message** -Methode senden. Weitere Informationen finden Sie unter [Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md)".

**So zeigen Sie eine Fehlermeldung innerhalb einer benutzerdefinierten Aktion mithilfe einer DLL an**

1.  Die benutzerdefinierte Aktion sollte " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " aufrufen und die Parameter " *hinstall*", " *emessagetype*" und " *hrecord*" übergeben. Das Handle für die Installation, [benutzerdefinierter Aktionstyp 19](custom-action-type-19.md), kann für die benutzerdefinierte Aktion bereitgestellt werden, wie unter [zugreifen auf die aktuelle Installer-Sitzung von innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md) oder über [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) oder [**msiopenpackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)beschrieben.
2.  Der Parameter *emessagetype* muss einen der Nachrichten Typen angeben, wie in [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)aufgeführt.
3.  Der *hrecord* -Parameter der [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion hängt vom Nachrichtentyp ab. Siehe [Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md)". Wenn die Nachricht formatierte Daten enthält, geben Sie die Nachricht in die [Fehler](error-table.md) Tabelle ein. verwenden Sie hierzu die unter [formatierte](formatted.md)Formatierung.

Um eine Fehlermeldung von einer benutzerdefinierten Aktion zu senden, die [Skripts](scripts.md)verwendet, kann die benutzerdefinierte Aktion die [**Message**](session-message.md) -Methode des [**Session**](session-object.md) -Objekts aufzurufen.

**So zeigen Sie eine Fehlermeldung innerhalb einer benutzerdefinierten Aktion mithilfe eines Skripts an**

1.  Die benutzerdefinierte Aktion sollte die [**Message**](session-message.md) -Methode des [**Session**](session-object.md) -Objekts aufzurufen und die Parameter *Art* und *Datensatz* übergeben.
2.  In der *Parameterart* sollte einer der Nachrichten Typen angegeben werden, die in der [**Message**](session-message.md) -Methode aufgeführt sind.
3.  Der *Datensatz* -Parameter der [**Message**](session-message.md) -Methode hängt vom Nachrichtentyp ab. Wenn die Nachricht formatierte Daten enthält, geben Sie die Nachricht in die [Fehler](error-table.md) Tabelle ein. verwenden Sie hierzu die unter [formatierte](formatted.md)Formatierung.

Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) verwenden, können keine Nachricht senden, indem Sie [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) oder die [**Message**](session-message.md) -Methode aufrufen, da Sie kein Handle für die Installation abrufen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md)
</dt> </dl>

 

 



