---
description: Der Zugriff auf COM+-Anwendungen, die als XML-Webdienste verfügbar gemacht werden, wird vom IIS-Webserver gesteuert, der die eingehenden Anforderungen verarbeitet.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Sichern von XML-Webdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343196"
---
# <a name="securing-xml-web-services"></a>Sichern von XML-Webdiensten

Der Zugriff auf COM+-Anwendungen, die als XML-Webdienste verfügbar gemacht werden, wird vom IIS-Webserver gesteuert, der die eingehenden Anforderungen verarbeitet. Sie können IIS auch so konfigurieren, dass die Kommunikation mit dem Aufrufer über einen sicheren Kanal erfolgen muss, der mit dem Secure Sockets Layer (SSL)-Protokoll festgelegt wurde.

> [!Note]  
> Ein geschützter XML-Webdienst unterstützt den WKO-Zugriff über WSDL nicht. Stattdessen können Clients, auf denen die .NET Framework Version 1,1 installiert ist, im Modus "Cao" aufgerufen werden. Wenn Clients von Drittanbietern über WSDL auf Ihren XML-Webdienst zugreifen müssen, müssen Sie den anonymen Zugriff zulassen.

 

> [!Note]  
> Wenn Sie das SSL-Protokoll verwenden möchten, um einen sicheren Kommunikationskanal einzurichten, müssen Sie ein SSL-Zertifikat abrufen und installieren.

 

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Führen Sie die folgenden Schritte aus, um den Authentifizierungsmechanismus für einen XML-Webdienst auszuwählen:

1.  Klicken Sie mit der rechten Maustaste auf das Symbol **Arbeitsplatz** auf Ihrem Desktop, und klicken Sie auf **Verwalten**.

2.  Suchen Sie unter **Dienste und Anwendungen** und **Internet Informationsdienste** das Symbol, das dem virtuellen Stammverzeichnis für den XML-Webdienst entspricht. Klicken Sie mit der rechten Maustaste auf das Verzeichnis Symbol, und wählen Sie **Eigenschaften**.

3.  Suchen Sie auf der Registerkarte **Verzeichnis Sicherheit** des Dialog Felds Eigenschaften nach **Authentifizierung und Zugriffs Steuerung** , und klicken Sie auf die entsprechende Schaltfläche **Bearbeiten** .

4.  Verwenden Sie im Dialogfeld **Authentifizierungsmethoden** unter **Authentifizierter Zugriff** die Kontrollkästchen, um die Authentifizierungsmechanismen auszuwählen, die Sie zulassen möchten. Klicken Sie auf **OK**.

    > [!Note]  
    > Sie können IIS zum Authentifizieren von Aufrufern konfigurieren, indem Sie eine der folgenden Optionen im Dialogfeld IIS- **Authentifizierungsmethoden** verwenden: **integrierte Windows-Authentifizierung**, Digestauthentifizierung **für Windows-Domänen Server**, Standard **Authentifizierung (Kennwort wird als Klartext gesendet)** oder **.NET Passport-Authentifizierung**. Sie können auch anonymen Zugriff zulassen.

     

5.  Klicken Sie im Dialogfeld "Eigenschaften" auf **OK**.

Um einen nicht sicheren, anonymen Zugriff auf einen XML-Webdienst zuzulassen, führen Sie die folgenden Schritte aus:

1.  Klicken Sie mit der rechten Maustaste auf das Symbol **Arbeitsplatz** auf Ihrem Desktop, und klicken Sie auf **Verwalten**.

2.  Suchen Sie unter **Dienste und Anwendungen** und **Internet Informationsdienste** das Symbol, das dem virtuellen Stammverzeichnis für den XML-Webdienst entspricht. Klicken Sie mit der rechten Maustaste auf das Verzeichnis Symbol, und wählen Sie **Eigenschaften**.

3.  Suchen Sie auf der Registerkarte **Verzeichnis Sicherheit** des Dialog Felds Eigenschaften nach **Authentifizierung und Zugriffs Steuerung**, und klicken Sie auf die entsprechende Schaltfläche **Bearbeiten** . Aktivieren Sie das Kontrollkästchen **anonymen Zugriff aktivieren** . Klicken Sie auf **OK**.

4.  Suchen Sie im Dialogfeld Eigenschaften auf der Registerkarte **Verzeichnis Sicherheit** die Schaltfläche **sichere Kommunikation** , und klicken Sie auf die entsprechende Schaltfläche **Bearbeiten** . Deaktivieren Sie das Kontrollkästchen **Secure Channel (SSL) erforderlich** . Klicken Sie auf **OK**.

5.  Klicken Sie im Dialogfeld "Eigenschaften" auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="additional-security-considerations"></a>Weitere Überlegungen zur Sicherheit

Wenn Sie einen sicheren Kanal benötigen, können Sie die Vertraulichkeit der ausgetauschten Daten schützen, indem Sie die Kommunikation zwischen dem Client und dem XML-Webdienst verschlüsseln. Wenn Sie die Authentifizierung mithilfe von Klartext-Kenn Wörtern zulassen, benötigen Sie einen sicheren Kanal, um zu verhindern, dass Kenn Wörter im Netzwerk verfügbar gemacht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im Modus "Cao"](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Sicherheitsüberlegungen für COM+-SOAP-Dienste](com--soap-service-security-considerations.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> </dl>

 

 



