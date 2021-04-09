---
description: Wenn Sie den com+-Ereignis Dienst verwenden, müssen Sie Maßnahmen ergreifen, um sicherzustellen, dass alle in einem Ereignis enthaltenen vertraulichen Informationen nicht gefährdet sind.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Sicherheitsüberlegungen für COM+-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958629"
---
# <a name="com-events-security-considerations"></a>Sicherheitsüberlegungen für COM+-Ereignisse

Wenn Sie den com+-Ereignis Dienst verwenden, müssen Sie Maßnahmen ergreifen, um sicherzustellen, dass alle in einem Ereignis enthaltenen vertraulichen Informationen nicht gefährdet sind.

Ereignis Herausgeber sollten bedenken, dass jede Partei, die in den com+-Katalog schreiben kann, Ihre Ereignisse abonnieren kann. Wenn die in einem Ereignis Klassenobjekt enthaltenen Informationen sensibel sind, sollten Sie daher mithilfe des Verwaltungs Tools Komponenten Dienste überprüfen, ob die Kommunikation mit Abonnenten für die Anwendung, die die Ereignis Klassen Komponenten enthält, verschlüsselt ist. (Wählen Sie im Eigenschaften Blatt der com+-Anwendung auf der Registerkarte **Sicherheit** die Option **Paket Datenschutz** als **Authentifizierungs Ebene für die Einstellung Aufrufe aus** .) Außerdem sollten Sie [Ereignis Filter](filtering-events-in-com-.md) verwenden, um sicherzustellen, dass Ereignisse nur an die entsprechenden Abonnenten übermittelt werden.

Ereignis Abonnenten sollten bedenken, dass eine böswillige Partei mit Zugriff auf Ihr Netzwerk und das Wissen Ihres Ereignis Klassen Objekts falsche Ereignisse erstellen könnte. Daher sollten Sie die [rollenbasierte Sicherheit](role-based-security-administration.md) verwenden, um sicherzustellen, dass Aufrufer der Methoden des Ereignis Klassen Objekts über die entsprechenden Anmelde Informationen verfügen, um die von der Implementierung beschriebenen Aktionen auszuführen.

Verwenden Sie zum Schutz von Verlegern und Abonnenten den com+-Ereignis Dienst in einem privaten Netzwerk vertrauenswürdiger Hosts, die von einer Firewall aus dem Internet isoliert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Sicherheit](com--security.md)
</dt> <dt>

[Filtern von Ereignissen in com+](filtering-events-in-com-.md)
</dt> <dt>

[Das com+-Ereignis Klassenobjekt](the-com--event-class-object.md)
</dt> </dl>

 

 



