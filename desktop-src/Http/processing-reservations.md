---
title: Verarbeitungs Reservierungen
description: Reservierungen für Teile des URL-Namespace werden vom Systemadministrator vorgenommen und im permanenten Reservierungs Speicher abgelegt.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391190"
---
# <a name="processing-reservations"></a>Verarbeitungs Reservierungen

Reservierungen für Teile des URL-Namespace werden vom Systemadministrator vorgenommen und im permanenten Reservierungs Speicher abgelegt. Der Stamm des URL-Namespace für http ist der Systemadministrator. Für alle Host-und Port Werte werden die beiden folgenden Reservierungen immer im Stamm des **relativeUri** -Namespace angenommen.



| Reservierter Namespace                 | Reserviert für              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | LocalSystem-Administrator |
| https:// <host> :<port>/ | LocalSystem-Administrator |



 

Diese impliziten Reservierungen können nicht entfernt werden. Es ist jedoch möglich, explizite Stamm Reservierungen an andere Benutzer zu delegieren. Durch Reservierungen wie die folgenden werden solche Delegierungen erstellt:



| Reservierter Namespace        | Reserviert für |
|---------------------------|--------------|
| `https://+:80/`           | UserA, userc |
| `https://adatum.com:443/` | UserB        |



 

Wenn diese Delegierten Reservierungen vom Systemadministrator entfernt werden, wird der Besitz des-Namespaces auf die implizite Reservierung der entsprechenden Host-und Port Werte zurückgesetzt.

 

 




