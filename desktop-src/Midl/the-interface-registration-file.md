---
title: Die Schnittstellen Registrierungsdatei
description: Die Schnittstellen Registrierungsdatei sammelt Informationen, die bei der Registrierung von in einer DLL-oder exe-Datei verpackten com-Schnittstellen helfen.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- Schnittstellen Registrierungsdatei (Mitte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340491"
---
# <a name="the-interface-registration-file"></a>Die Schnittstellen Registrierungsdatei

Die Schnittstellen Registrierungsdatei sammelt Informationen, die bei der Registrierung von in einer DLL-oder exe-Datei verpackten com-Schnittstellen helfen. Die Schnittstellen Registrierungsdatei unterscheidet sich von anderen generierten Dateien, da Sie Informationen aus der Kompilierung verschiedener IDL-Dateien erfassen kann. Jeder mittlere compilerlauf für COM-Schnittstellen sucht zuerst nach einer vorhandenen Datei "dlldata. c". wenn die Datei nicht gefunden wird, wird eine neue Datei "dlldata. c" erstellt. Wenn eine dlldata. c-Datei gefunden wird, werden Informationen über die aktuelle IDL hinzugefügt (sofern nicht vorhanden) oder ersetzt.

Die Schnittstellen Registrierungsdatei wird auf sichere Weise in einer Multiprozessorumgebung generiert oder aktualisiert, da parallele Mittel l-Kompilierungen daran gehindert werden, gleichzeitig in die Datei zu schreiben. Da jede dlldata. c-Datei entweder von der Buildumgebung oder vom Benutzer als schreibgeschützt gekennzeichnet werden kann, implementiert der mittlerer l-Compiler einen Timeout Ansatz, der auf eine Datei wartet, die nicht geöffnet werden kann, und gibt eine entsprechende Fehlermeldung aus, wenn das Timeout abläuft.

Der Standardname für die von einer Eingabedatei generierte Schnittstellen Registrierungsdatei lautet "dlldata. c". Der [**/dlldata**](-dlldata.md) -Compilerschalter kann verwendet werden, um den Standardnamen der Datei zu überschreiben. Das Überschreiben des Standard namens der Schnittstellen Registrierungsdatei ist besonders nützlich, wenn sich einige IDL-Dateien, die in eine gemeinsame Binärdatei gepackt sind, in verschiedenen Verzeichnissen befinden

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln und Registrieren einer Proxy-dll](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 