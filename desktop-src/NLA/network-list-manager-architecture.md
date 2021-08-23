---
title: Architektur des Netzwerklisten-Managers
description: Architektur des Netzwerklisten-Managers
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ecbb36c5421bc7e3057c43feb10f92400493b306ecb21502a541c1bb4cba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685645"
---
# <a name="network-list-manager-architecture"></a>Architektur des Netzwerklisten-Managers

Der Netzwerklisten-Manager wird als Dienst im Kontext des Svchost.exe ausgeführt und während des Computerstartvorgangs gestartet. Der Netzwerklisten-Manager-Dienst verwaltet eine Tabelle der verfügbaren Netzwerke und Netzwerkattribute, die von Anwendungen über die Network List Manager-API abgerufen werden. Der Netzwerklisten-Manager bietet grundlegende Funktionen zum Filtern und Abfragen des Netzwerklisten-Manager-Diensts nach bestimmten Netzwerken und zum Abrufen der Attribute dieser Netzwerke. Das folgende Diagramm zeigt die Architektur des Netzwerklisten-Managers und die Interaktion zwischen dem Netzwerklisten-Manager-Dienst und der Clientanwendung.

![Diagramm zur Netzwerkbewusstseinsarchitektur](images/architecture.png)

 

 




