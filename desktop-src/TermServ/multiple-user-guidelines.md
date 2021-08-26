---
title: Richtlinien für mehrere Benutzer
description: Richtlinien für die Entwicklung von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste-Umgebung.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc598042530ab59c0c8932522185ce5a9d0d3dce04cabce44239c3c81b79d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988850"
---
# <a name="multiple-user-guidelines"></a>Richtlinien für mehrere Benutzer

Die folgenden Abschnitte enthalten Richtlinien für die Entwicklung von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste-Umgebung.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Anwendungseinrichtung](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

Das Installieren einer Anwendung für einen einzelnen Benutzer kann probleme in einer Umgebung mit mehreren Benutzern Remotedesktopdienste verursachen.

</dd> <dt>

[Speichern von benutzerspezifischen Informationen](storing-user-specific-information.md)
</dt> <dd>

Anwendungen sollten benutzerspezifische Informationen an benutzerspezifischen Speicherorten speichern, die von den globalen, auf alle Benutzer bezogenen Informationen getrennt sind.

</dd> <dt>

[Kernelobjektnamespaces](kernel-object-namespaces.md)
</dt> <dd>

Remotedesktopdienste verwendet mehrere Namespaces für Kernelobjekte. ein globaler Namespace wird hauptsächlich von Diensten in Client-/Serveranwendungen verwendet.

</dd> <dt>

[IP-Adressen und Computernamen](ip-addresses-and-computer-names.md)
</dt> <dd>

Es darf nicht davon ausgegangen werden, dass der Computername oder die dem Computer zugewiesene IP-Adresse mit einem einzelnen Benutzer zusammenhängen, da mehrere Benutzer gleichzeitig an einem Remote Desktop Session Host-Server (RD Session Host) angemeldet sein können.

</dd> </dl>

Sperren Sie wie immer Dateien und Datenbanken, während Sie Änderungen vornehmen, um unbeabsichtigte Datenverluste zu verhindern.

Ihre Anwendung darf keine Laufzeitanwendungsdateien sperren, die keine Benutzerdateien sind. Gesperrte Laufzeitdateien können dazu führen, dass mehrere Instanzen der Anwendung oder Prozesse in der Anwendung, z. B. Assistenten, nicht ausgeführt werden. Eine gute Möglichkeit, zu testen, welche Dateien Laufzeitanwendungsdateien sind, besteht darin, nachzuverfolgen, welche Dateien vom Anwendungssetup installiert werden. Benutzerspezifische Dateien werden nur selten vom Setup installiert. Daher sind die meisten vom Setup installierten Dateien Laufzeitanwendungsdateien.

 

 




