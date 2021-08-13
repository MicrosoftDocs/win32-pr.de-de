---
description: Der Zugriff auf COM+-Anwendungen, die als XML-Webdienste verfügbar gemacht werden, wird vom IIS-Webserver gesteuert, der die eingehenden Anforderungen verarbeitet.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Sichern von XML-Webdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc49a096def7fdca3f508ca590cd23df0fbf2e92fd816ba55300931122361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546963"
---
# <a name="securing-xml-web-services"></a>Sichern von XML-Webdiensten

Der Zugriff auf COM+-Anwendungen, die als XML-Webdienste verfügbar gemacht werden, wird vom IIS-Webserver gesteuert, der die eingehenden Anforderungen verarbeitet. Sie können IIS auch so konfigurieren, dass die Kommunikation mit dem Aufrufer über einen sicheren Kanal erfolgt, der mithilfe des SSL-Protokolls (Secure Sockets Layer) eingerichtet wurde.

> [!Note]  
> Ein gesicherter XML-Webdienst unterstützt den WKO-Zugriff über WSDL nicht. Stattdessen können Clients, die die .NET Framework Version 1.1 installiert haben, sie im CAO-Modus aufrufen. Wenn Drittanbieterclients über WSDL auf Ihren XML-Webdienst zugreifen müssen, müssen Sie anonymen Zugriff zulassen.

 

> [!Note]  
> Um das SSL-Protokoll zum Einrichten eines sicheren Kommunikationskanals zu verwenden, müssen Sie ein SSL-Zertifikat abrufen und installieren.

 

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Um den Authentifizierungsmechanismus für einen XML-Webdienst auszuwählen, führen Sie die folgenden Schritte aus:

1.  Klicken Sie mit der rechten **Maustaste Arbeitsplatz** Symbol auf Ihrem Desktop, und klicken Sie auf **Verwalten.**

2.  Suchen **Sie unter Dienste und Anwendungen** und **Internetinformationsdienst** das Symbol, das dem virtuellen Stammverzeichnis für Ihren XML-Webdienst entspricht. Klicken Sie mit der rechten Maustaste auf das Verzeichnissymbol, und wählen Sie **Eigenschaften aus.**

3.  Suchen Sie **im Eigenschaftendialogfeld** auf der Registerkarte Verzeichnissicherheit nach Authentifizierung und **Zugriffssteuerung,** und klicken Sie auf **die entsprechende Schaltfläche** Bearbeiten.

4.  Aktivieren Sie **im Dialogfeld Authentifizierungsmethoden** unter **Authentifizierter** Zugriff die Kontrollkästchen, um die Authentifizierungsmechanismen auszuwählen, die Sie zulassen möchten. Klicken Sie auf **OK**.

    > [!Note]  
    > Sie können IIS so konfigurieren, dass Aufrufer mithilfe  einer der folgenden Optionen im Dialogfeld IIS-Authentifizierungsmethoden authentifiziert werden: integrierte **Windows-Authentifizierung,** Digestauthentifizierung für Windows-Domänenserver, Standardauthentifizierung (Kennwort wird als Klartext **gesendet)** oder  **.NET Passport-Authentifizierung**. Sie können auch anonymen Zugriff zulassen.

     

5.  Klicken Sie im Eigenschaftendialogfeld auf **OK.**

Um einen unsicheren, anonymen Zugriff auf einen XML-Webdienst zu ermöglichen, führen Sie die folgenden Schritte aus:

1.  Klicken Sie mit der rechten **Maustaste Arbeitsplatz** Symbol auf Ihrem Desktop, und klicken Sie auf **Verwalten.**

2.  Suchen **Sie unter Dienste und Anwendungen** und **Internetinformationsdienst** das Symbol, das dem virtuellen Stammverzeichnis für Ihren XML-Webdienst entspricht. Klicken Sie mit der rechten Maustaste auf das Verzeichnissymbol, und wählen Sie **Eigenschaften aus.**

3.  Suchen Sie **im Eigenschaftendialogfeld** auf der Registerkarte Verzeichnissicherheit nach Authentifizierung und **Zugriffssteuerung,** und klicken Sie auf die **entsprechende Schaltfläche** Bearbeiten. Aktivieren Sie das **Kontrollkästchen Anonymen Zugriff** aktivieren. Klicken Sie auf **OK**.

4.  Suchen Sie **im Eigenschaftendialogfeld** auf der Registerkarte Verzeichnissicherheit nach **Sichere Kommunikation,** und klicken Sie auf die **entsprechende Schaltfläche** Bearbeiten. Deaktivieren Sie das **Kontrollkästchen Secure Channel (SSL)** erforderlich. Klicken Sie auf **OK**.

5.  Klicken Sie im Eigenschaftendialogfeld auf **OK.**

## <a name="visual-basic"></a>Visual Basic

Nicht anwendbar.

## <a name="cc"></a>C/C++

Nicht anwendbar.

## <a name="additional-security-considerations"></a>Weitere Überlegungen zur Sicherheit

Durch die Anforderung eines sicheren Kanals können Sie die Vertraulichkeit der ausgetauschten Daten schützen, indem Sie die Kommunikation zwischen dem Client und Ihrem XML-Webdienst verschlüsseln. Wenn Sie die Authentifizierung mit Klartextkennwörtern zulassen, sollten Sie einen sicheren Kanal benötigen, um zu vermeiden, dass Kennwörter im Netzwerk verfügbar gemacht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im CAO-Modus](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Sicherheitsüberlegungen zum COM+-SOAP-Dienst](com--soap-service-security-considerations.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> </dl>

 

 



