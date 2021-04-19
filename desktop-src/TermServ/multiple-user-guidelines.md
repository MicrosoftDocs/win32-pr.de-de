---
title: Richtlinien für mehrere Benutzer
description: Richtlinien für die Entwicklung von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste Umgebung.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339235"
---
# <a name="multiple-user-guidelines"></a>Richtlinien für mehrere Benutzer

In den folgenden Abschnitten finden Sie Richtlinien zum Entwickeln von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste Umgebung.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Anwendungseinrichtung](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

Durch die Installation einer Anwendung für einen einzelnen Benutzer können Probleme in einer mehr Benutzer Remotedesktopdienste Umgebung entstehen.

</dd> <dt>

[Speichern von benutzerspezifischen Informationen](storing-user-specific-information.md)
</dt> <dd>

Anwendungen sollten benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, die von den globalen, auf alle Benutzer bezogenen Informationen getrennt sind.

</dd> <dt>

[Kernelobjektnamespaces](kernel-object-namespaces.md)
</dt> <dd>

Remotedesktopdienste verwendet mehrere Namespaces für Kernel Objekte. ein globaler Namespace wird hauptsächlich von Diensten in Client/Server-Anwendungen verwendet.

</dd> <dt>

[IP-Adressen und Computernamen](ip-addresses-and-computer-names.md)
</dt> <dd>

Es darf nicht davon ausgegangen werden, dass der Computername oder die dem Computer zugewiesene IP-Adresse mit einem einzelnen Benutzer zusammenhängen, da mehrere Benutzer gleichzeitig an einem Remote Desktop Session Host-Server (RD Session Host) angemeldet sein können.

</dd> </dl>

Sperren Sie wie immer Dateien und Datenbanken, während Sie Änderungen vornehmen, um unbeabsichtigte Datenverluste zu verhindern.

Die Anwendung darf keine Lauf Zeit Anwendungs Dateien sperren, bei denen es sich nicht um benutzerspezifische Dateien handelt. Gesperrte Laufzeitdateien können die Ausführung mehrerer Instanzen der Anwendung oder der Prozesse unter der Anwendung, z. b. Assistenten, behalten. Eine gute Möglichkeit, um zu testen, welche Dateien Lauf Zeit Anwendungs Dateien sind, besteht darin, zu verfolgen, welche Dateien vom Anwendungs Setup installiert werden. Benutzerspezifische Dateien werden nur selten vom-Setup installiert. Daher sind die meisten Dateien, die durch das-Setup installiert werden, Lauf Zeit Anwendungs Dateien.

 

 




