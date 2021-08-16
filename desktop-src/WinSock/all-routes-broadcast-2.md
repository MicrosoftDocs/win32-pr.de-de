---
description: Eine allgemeine Übertragung über das Internet wird erreicht, indem die Felder sa netnum und sa nodenum auf binäre Felder \_ \_ (1) setzen.
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Übertragung aller Routen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a5f0ba1e900dd390610a3bd3af2f779d523ae4a08973596e7da6b8331acc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322720"
---
# <a name="all-routes-broadcast"></a>Übertragung aller Routen

Eine allgemeine Übertragung über das Internet wird erreicht, indem die **Felder sa \_ netnum** und **sa \_ nodenum** auf binäre Felder (1) setzen. Der Dienstanbieter übersetzt diese Anforderung in ein Typ-20-Paket, das von IPX-Routern erkannt und weitergeleitet wird. Das Paket besucht alle Subnetze und kann mehrmals dupliziert werden. Empfänger müssen mehrere doppelte Kopien des Datagramms verarbeiten.

Die Verwendung dieses Broadcasttyps ist bei Netzwerkadministratoren unpopulär, daher sollte seine Verwendung extrem eingeschränkt sein. Viele Router deaktivieren diese Art von Broadcast, und Teile des Subnetzes bleiben für das Paket unsichtbar.

 

 



