---
description: Eine allgemeine Übertragung über das Internet erfolgt durch Festlegen der \_ Felder SA netnum und SA \_ nodenum auf Binärdateien (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Alle Routen Broadcast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484963"
---
# <a name="all-routes-broadcast"></a>Alle Routen Broadcast

Eine allgemeine Übertragung über das Internet erfolgt durch Festlegen der Felder **sa \_ netnum** und **sa \_ nodenum** auf Binärdateien (1). Der Dienstanbieter übersetzt diese Anforderung in ein Typ-20-Paket, das IPX-Router erkennen und weiterleiten. Das Paket besucht alle Subnetze und kann mehrmals dupliziert werden. Empfänger müssen mehrere doppelte Kopien des Datagramms verarbeiten.

Die Verwendung dieses Broadcast Typs ist für Netzwerkadministratoren unpopulär, daher sollte die Verwendung sehr eingeschränkt sein. Viele Router deaktivieren diese Art von Broadcast, sodass Teile des Subnetzes nicht für das Paket unsichtbar sind.

 

 



