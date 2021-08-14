---
title: Verarbeiten von Reservierungen
description: Reservierungen für Teile des URL-Namespaces werden vom Systemadministrator vorgenommen und im persistenten Reservierungsspeicher platziert.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f0e38f5994687bfe26d1334300c0aa7fbbd3f8096abcf60e6c523e7d030a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393762"
---
# <a name="processing-reservations"></a>Verarbeiten von Reservierungen

Reservierungen für Teile des URL-Namespaces werden vom Systemadministrator vorgenommen und im persistenten Reservierungsspeicher platziert. Der Stamm des URL-Namespace für HTTP befindet sich im Besitz des Systemadministrators. Für alle Host- und Portwerte werden die folgenden beiden Reservierungen immer im Stammverzeichnis des **relativeUri-Namespaces** angenommen.



| Reservierter Namespace                 | Reserviert für              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | LocalSystem Administrator |
| https:// <host> :<port>/ | LocalSystem Administrator |



 

Diese impliziten Reservierungen können nicht entfernt werden. Es ist jedoch möglich, explizite Stammreservierungen an andere Benutzer zu delegieren. Reservierungen wie die folgenden würden solche Delegationen erstellen:



| Reservierter Namespace        | Reserviert für |
|---------------------------|--------------|
| `https://+:80/`           | UserA, UserC |
| `https://adatum.com:443/` | Benutzerb        |



 

Wenn diese delegierten Reservierungen vom Systemadministrator entfernt werden, wird der Besitz des Namespace auf die implizite Reservierung für die entsprechenden Host- und Portwerte zurückgesetzt.

 

 




