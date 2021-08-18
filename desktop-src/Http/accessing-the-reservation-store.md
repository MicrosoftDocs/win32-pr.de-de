---
title: Zugreifen auf die Store
description: Die HTTP-Server-API verwaltet die Namespacereservierungsliste für alle Benutzer auf dem Computer.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Zugreifen auf den Reservierungs-Store HTTP
- Reservierung Store HTTP, Zugreifen auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f9244fd4513517793bf85d205308fc49ac2d8ca0a246c17a68c730d1c76168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015018"
---
# <a name="accessing-the-reservation-store"></a>Zugreifen auf die Store

Die HTTP-Server-API verwaltet die Namespacereservierungsliste für alle Benutzer auf dem Computer. Ein Reservierungseintrag besteht aus einem [UrlPrefix](urlprefix-strings.md) und der entsprechenden ACL. Jedes UrlPrefix im Speicher verfügt über eine ACL, die alle Benutzer auflistet, die sich für den Empfang von Anforderungen für den Namespace registrieren dürfen. Benutzer mit Delegierungsberechtigungen können Teilstruktur des Namespace, den sie besitzen, an andere Benutzer delegieren oder vorhandene Reservierungen mithilfe der Konfigurations-APIs löschen.

Um dem persistenten Reservierungsspeicher eine Reservierung hinzuzufügen, ruft die Anwendung die [**Funktion HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) auf, bei der der Konfigurations-ID-Parameter auf den **Wert HttpServiceConfigUrlAclInfo festgelegt** ist. Die HTTP-Server-API überprüft den Besitz des Namespace und der Benutzer-ID, bevor dem Speicher eine Reservierung hinzugefügt wird.

Die HTTP-Server-API stellt auch Funktionen zum Abfragen und Löschen der Dienstkonfigurationen für URL-Namespaces bereit. Die [**Aufgerufene HttpQueryServiceConfiguration-Funktion**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) mit dem Konfigurations-ID-Parameter, der auf die **HttpServiceConfigUrlAclInfo-Wertabfragen** festgelegt ist, und die [**HttpDeleteServiceConfiguration-Funktion**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) wird im URL-Namespacespeicher gelöscht.

 

 




