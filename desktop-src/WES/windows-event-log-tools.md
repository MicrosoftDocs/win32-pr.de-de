---
title: Windows Ereignisprotokolltools
description: Windows Das Ereignisprotokoll bietet die folgenden Tools, die Sie zum Erstellen Ihres Anbieters verwenden.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7a0aef85e85e096381b65d41458f1cb955ba9701452498d21c45ff25cb3058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587257"
---
# <a name="windows-event-log-tools"></a>Windows Ereignisprotokolltools

Windows Das Ereignisprotokoll bietet die folgenden Tools, die Sie zum Erstellen Ihres Anbieters verwenden.



| Tool                                                           | BESCHREIBUNG                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md)  | Ein Befehlszeilenprogramm zum Kompilieren von Instrumentierungsmanifesten und Meldungstextdateien. |
| WevtUtil.exe                                                   | Ein Befehlszeilenprogramm, das hauptsächlich zum Registrieren Ihres Anbieters auf dem Computer verwendet wird. Sie können sie auch verwenden, um Metadateninformationen über den Anbieter, seine Ereignisse und die Kanäle, in denen Ereignisse protokolliert werden, zu erhalten und Ereignisse aus einem Kanal oder einer Protokolldatei abfragt. Das WevtUtil.exe ist in %windir% \\ System32 enthalten. Geben Sie "wevtutil /?" ein, um Nutzungsinformationen zu erhalten. an einer Eingabeaufforderung.<br/> Dieser Befehl ist auf Mitglieder der Gruppe Administratoren beschränkt und muss mit erhöhten Rechten ausgeführt werden.|
