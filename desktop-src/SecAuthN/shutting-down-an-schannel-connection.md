---
description: Beenden einer SChannel-Verbindung
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Beenden einer SChannel-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749601"
---
# <a name="shutting-down-an-schannel-connection"></a>Beenden einer SChannel-Verbindung

Wenn ein Client oder Server mit einer Verbindung fertig ist, muss er heruntergefahren werden. Die andere Partei muss wiederum das Herunterfahren erkennen und die Verbindung löschen.

**So fahren Sie eine SChannel-Verbindung herunter**

1.  Wenden Sie die [**applycontroltoken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) -Funktion an, und geben Sie das SChannel \_ Shutdown-Steuerungs Token an.
2.  Nachdem Sie einen SEK \_ \_ .-Rückgabewert von [**applycontroltoken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)erhalten haben, können Sie die Funktion [**InitializeSecurityContext (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (Clients) oder [**Accept tsecuritycontext (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (Server) abrufen, indem Sie leere Puffer übergeben.
3.  Gehen Sie so vor, als ob die Anwendung eine neue Verbindung erstellt hätte, bis die Funktion SEK \_ . I- \_ Kontext \_ abgelaufen oder SEK \_ . OK zurückgibt \_ , um anzugeben, dass die Verbindung heruntergefahren wird.
4.  Senden Sie ggf. die endgültigen Ausgabeinformationen an den Remote Anbieter.
5.  Ruft den [**Delta Context-Kontext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) auf, um die von der Verbindung gehaltenen Ressourcen freizugeben.

## <a name="recognizing-a-shutdown"></a>Erkennen eines herunter Fahrens

Die Funktion [**DecryptMessage (SChannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) gibt Sekunde zurück, \_ Wenn der \_ \_ Nachrichten Absender die Verbindung beendet hat. Nachdem Sie diesen Rückgabewert erhalten haben, führen Sie das Verfahren zum Herunterfahren einer SChannel-Verbindung weiter oben in diesem Thema aus.

 

 
