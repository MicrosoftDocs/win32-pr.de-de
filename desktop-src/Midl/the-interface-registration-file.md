---
title: Die Schnittstellenregistrierungsdatei
description: Die Schnittstellenregistrierungsdatei sammelt Informationen, die bei der Registrierung von COM-Schnittstellen helfen, die in eine DLL- oder EXE-Datei gepackt sind.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- Schnittstellenregistrierungsdatei MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a5541a5e60b1903364236f86dcf1845a5e1ac153fc91b47bacf9f553a9a109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806178"
---
# <a name="the-interface-registration-file"></a>Die Schnittstellenregistrierungsdatei

Die Schnittstellenregistrierungsdatei sammelt Informationen, die bei der Registrierung von COM-Schnittstellen helfen, die in eine DLL- oder EXE-Datei gepackt sind. Die Schnittstellenregistrierungsdatei ist anders als andere generierte Dateien, da sie Informationen aus der Kompilierung mehrerer verschiedener IDL-Dateien sammeln kann. Jeder MIDL-Compiler, der für COM-Schnittstellen ausgeführt wird, sucht zuerst nach einer vorhandenen dlldata.c-Datei, und wenn die Datei nicht gefunden wird, wird eine neue dlldata.c-Datei erstellt. Wenn eine dlldata.c-Datei gefunden wird, werden Informationen zur aktuellen IDL hinzugefügt (falls nicht vorhanden) oder ersetzt.

Die Schnittstellenregistrierungsdatei wird in einer Umgebung mit mehreren Prozessoren sicher generiert oder aktualisiert, da parallele MIDL-Kompilierungen nicht gleichzeitig in die Datei schreiben können. Da jede dlldata.c-Datei entweder von der Buildumgebung oder vom Benutzer als schreibgeschützt markiert werden kann, implementiert der MIDL-Compiler einen Timeoutansatz zum Warten auf eine Datei, die nicht geöffnet werden kann, und gibt eine entsprechende Fehlermeldung aus, wenn das Timeout abläuft.

Der Standardname für die Aus einer Eingabedatei generierte Schnittstellenregistrierungsdatei ist dlldata.c. Der [**Compilerschalter /dlldata**](-dlldata.md) MIDL kann verwendet werden, um den Standardnamen der Datei zu überschreiben. Das Überschreiben des Standardnamens der Schnittstellenregistrierungsdatei ist besonders nützlich, wenn sich einige in eine gemeinsame Binärdatei gepackte IDL-Dateien in unterschiedlichen Verzeichnissen befinden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen und Registrieren einer Proxy-DLL](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 