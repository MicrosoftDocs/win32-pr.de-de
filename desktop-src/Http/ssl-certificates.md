---
title: SSL-Zertifikate
description: Secure Sockets Layer (SSL) ist ein Standard zum Sichern von Internet Verbindungen und wird verwendet, um das Auslassen von lausch im Netzwerk zu verhindern. Das SSL-Protokoll ermöglicht einem Client und einem Server, sich gegenseitig zu authentifizieren und Verschlüsselungsalgorithmen auszuhandeln.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "106339469"
---
# <a name="ssl-certificates"></a>SSL-Zertifikate

Secure Sockets Layer (SSL), auch bekannt als Transport Layer Security (TLS), ist ein Standard zum Sichern von Internet Verbindungen und wird verwendet, um das verhindern von lausch Angriffen im Netzwerk zu verhindern. Das SSL/TLS-Protokoll ermöglicht einem Client und einem Server, sich gegenseitig zu authentifizieren und Verschlüsselungsalgorithmen auszuhandeln.

SSL verwendet einen Verschlüsselungsschlüssel und einen Verschlüsselungsalgorithmus, um die HTTP-Verbindung zu sichern. Die Verschlüsselungsschlüssel sind in SSL-Zertifikaten enthalten, die sowohl vom Client als auch vom Server verwendet werden. Das Zertifikat ist in der Regel ein X. 509-Dokument ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)). Der Server stellt das SSL-Zertifikat für die Sitzung bereit und sendet das Zertifikat in der Hand Shake Phase an den Client. Der Client sendet das Zertifikat nur dann an den Server, wenn der Server eine Anforderung für ein Zertifikat an den Client sendet. Daher authentifiziert der Client den Server immer, aber der Server hat die Möglichkeit, den Client zu authentifizieren.

Server Zertifikate müssen im lokalen permanenten Speicher der HTTP-Server-API gespeichert werden, damit Sie bei jeder Erstellung einer sicheren Verbindung verwendet werden können. Jeder Zertifikat Speicher Eintrag enthält auch die IP-Adresse und den Port des Servers, den Zertifikat Hash (dient zum Signieren der Nachrichten) und die Anwendungs-ID. Die Anwendungs-ID wird verwendet, um die Anwendung zu identifizieren, die das Zertifikat besitzt.

System Administratoren können SSL-Serverzertifikat Informationen mit den Konfigurations-APIs speichern. Ein Verwaltungs Tool Ruft die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion auf und gibt den httpserviceconfigsslcertinfo-Wert für den Dienst Konfigurationsparameter an, um Informationen für ein SSL-Zertifikat festzulegen. Für jede IP-Adresse und jedes Port Paar auf dem Computer kann nur ein Serverzertifikat konfiguriert werden. Die HTTP-Server-API bietet auch [**Abfrage**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) -und [**Lösch**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) Funktionen, um auf vorhandene Zertifikate zuzugreifen oder diese zu löschen.

 

 




