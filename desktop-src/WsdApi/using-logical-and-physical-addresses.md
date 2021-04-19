---
description: 'WS-Discovery definiert die logische Adressierung mithilfe von URIs basierend auf dem urn: uuid:-Format.'
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: Verwenden von logischen und physischen Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356752"
---
# <a name="using-logical-and-physical-addresses"></a>Verwenden von logischen und physischen Adressen

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) definiert die logische Adressierung mithilfe von URIs basierend auf dem `urn:uuid:` Format. Der Zweck dieses Adressierungs Schemas besteht darin, die Identität des Geräts von seiner aktuellen IP-Adresse zu unterscheiden. Dieses Schema bietet im Wesentlichen die Funktionalität von DNS-Namen, ohne dass ein Namensserver erforderlich ist. [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) empfiehlt, dass Geräte dieses Adressierungs Schema verwenden.

Außerdem wird von DPWS empfohlen, dass Dienste physische (auch Transport-) Adressen verwenden. Dies ermöglicht es Clients, die keine systemeigene Unterstützung für WS-Discovery Adressierungs Mechanismen zur Kommunikation mit den DPWS-Diensten verwenden. Außerdem kann jeder Dienst seine Adressen definieren, was die Adressierung von Transport Ebenen für Geräte Implementierungen ermöglicht, die die Dienst Verteilung auf einer niedrigeren Ebene verwalten. Zum Schluss maximiert die Verwendung physischer Adressen die Interoperabilität.

Der Nachteil der physischen Adressierung besteht darin, dass die Geräte Implementierungen komplexer werden, da die aktuelle IP-Adresse oder Transport Adresse nachverfolgt werden muss und Geräte Metadaten entsprechend geändert werden müssen. Aus diesem Grund ist es für DPWS nicht erforderlich, dass für die Verwendung von Transport Adressen Dienste verwendet werden.

Wenn logische Adressen verwendet werden, gibt es einige Szenarien, in denen das Implementierungs Verhalten nicht definiert ist. In der WS-Discovery Spezifikation wird nicht beschrieben, was es bedeutet, dass sich ein Dienst bei einer logischen Adresse befinden muss. R1001 der WS-Discovery Spezifikation empfiehlt die Verwendung von WS-Discovery für gehostete Dienste aufgrund der zugeordneten Netzwerk Chatter.

Es wird nicht empfohlen, dass sich Dienste an logischen Adressen befinden, da dadurch die Interoperabilität verringert wird. Wenn eine Implementierung sich unbedingt an einer logischen Adresse befinden muss, sollte der Dienst dieselbe logische Adresse wie das Gerät verwenden. Wenn dies dem dispatchmodell auf dem Gerät zu viel Komplexität hinzufügt, empfiehlt es sich, die Dienste mithilfe von Verweis Parametern zu unterscheiden. WSDAPI sendet Nachrichten ordnungsgemäß an-Dienste, wenn Sie dieselbe Endpunkt Adresse wie das Gerät verwenden.

 

 



