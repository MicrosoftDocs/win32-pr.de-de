---
description: In diesem Abschnitt wird beschrieben, wie Sie Nachrichten von benutzerdefinierten Aktionen senden, die tatsächlich einen Teil der Installation ausführen, indem Sie eine Dynamic Link Library oder ein Skript aufrufen.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Zurückgeben von Fehlermeldungen aus benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c951b0e86d3120b989605572f15681582ac437fca5981852413331a3e63e684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869120"
---
# <a name="returning-error-messages-from-custom-actions"></a>Zurückgeben von Fehlermeldungen aus benutzerdefinierten Aktionen

In diesem Abschnitt wird beschrieben, wie Sie Nachrichten von benutzerdefinierten Aktionen senden, die tatsächlich einen Teil der Installation ausführen, indem Sie eine Dynamic Link Library oder ein Skript aufrufen. Beachten [Sie, dass der](custom-action-type-19.md) benutzerdefinierte Aktionstyp 19 nur eine angegebene Fehlermeldung sendet, einen Fehler zurückgibt und dann die Installation beendet. Der benutzerdefinierte Aktionstyp 19 führt keinen Teil der Installation aus.

Um eine Fehlermeldung von einer benutzerdefinierten Aktion zu senden, die eine [Dynamic Link Library](dynamic-link-libraries.md) (DLL) verwendet, rufen Sie mit der benutzerdefinierten Aktion [**MsiProcessMessage auf.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) Beachten Sie, dass benutzerdefinierte Aktionen, die von [einem DoAction ControlEvent](doaction-controlevent.md) gestartet werden, Nachrichten mit der [**Message-Methode**](session-message.md) senden können, aber keine Nachricht mit **MsiProcessMessage senden können.** Auf Systemen vor Windows Server 2003 können benutzerdefinierte Aktionen, die von einem DoAction ControlEvent gestartet werden, keine Nachrichten mit **der MsiProcessMessage-** oder **Message-Methode** senden. Weitere Informationen finden Sie unter [Senden von Nachrichten an Windows Installer mit msiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

**So zeigen Sie eine Fehlermeldung innerhalb einer benutzerdefinierten Aktion mithilfe einer DLL an**

1.  Die benutzerdefinierte Aktion sollte [**MsiProcessMessage aufrufen**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) und die Parameter *hInstall,* *eMessageType* und *hRecord übergeben.* Das Handle für die Installation( Benutzerdefinierter Aktionstyp [19](custom-action-type-19.md)) kann für die benutzerdefinierte Aktion bereitgestellt werden, wie [unter](accessing-the-current-installer-session-from-inside-a-custom-action.md) Zugreifen auf die aktuelle Installersitzung von innerhalb einer benutzerdefinierten Aktion oder von [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) oder [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)beschrieben.
2.  Der Parameter *eMessageType* sollte einen der Nachrichtentypen angeben, wie in [**MsiProcessMessage aufgeführt.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)
3.  Der *hRecord-Parameter* der [**MsiProcessMessage-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) hängt vom Nachrichtentyp ab. Siehe [Senden von Nachrichten an Windows Installer mit msiProcessMessage.](sending-messages-to-windows-installer-using-msiprocessmessage.md) Wenn die Nachricht formatierte Daten enthält, geben Sie die Meldung in die [Tabelle Fehler](error-table.md) ein, indem Sie die in [Formatierte beschriebene Formatierung verwenden.](formatted.md)

Um eine Fehlermeldung von einer benutzerdefinierten Aktion zu senden, die [Skripts](scripts.md)verwendet, kann die benutzerdefinierte Aktion die [**Message-Methode**](session-message.md) des [**Session-Objekts**](session-object.md) aufrufen.

**So zeigen Sie eine Fehlermeldung innerhalb einer benutzerdefinierten Aktion mithilfe eines Skripts an**

1.  Die benutzerdefinierte Aktion sollte die [**Message-Methode**](session-message.md) des [**Session-Objekts aufrufen**](session-object.md) und die *Parameterart und den Datensatz* *übergeben.*
2.  Die *Parameterart* sollte einen der nachrichtentypen angeben, die in der [**Message-Methode aufgeführt**](session-message.md) sind.
3.  Der *Record-Parameter* der [**Message-Methode**](session-message.md) hängt vom Nachrichtentyp ab. Wenn die Nachricht formatierte Daten enthält, geben Sie die Meldung in die [Tabelle Fehler](error-table.md) ein, indem Sie die in [Formatierte beschriebene Formatierung verwenden.](formatted.md)

Benutzerdefinierte Aktionen, die [ausführbare Dateien verwenden,](executable-files.md) können keine Nachricht senden, indem [**sie MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) oder die [**Message-Methode**](session-message.md) aufrufen, da sie kein Handle für die Installation erhalten können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md)
</dt> </dl>

 

 



