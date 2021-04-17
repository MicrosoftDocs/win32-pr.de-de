---
title: Windows-Ereignisprotokoll Tools
description: Das Windows-Ereignisprotokoll stellt die folgenden Tools bereit, die Sie zum Erstellen Ihres Anbieters verwenden können.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390097"
---
# <a name="windows-event-log-tools"></a>Windows-Ereignisprotokoll Tools

Das Windows-Ereignisprotokoll stellt die folgenden Tools bereit, die Sie zum Erstellen Ihres Anbieters verwenden können.



| Tool                                                           | BESCHREIBUNG                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md)  | Ein Befehlszeilen-Hilfsprogramm, mit dem Instrumentierungs Manifeste und Nachrichtentext Dateien kompiliert werden. |
| WevtUtil.exe                                                   | Ein Befehlszeilen-Hilfsprogramm, das hauptsächlich zum Registrieren Ihres Anbieters auf dem Computer verwendet wird. Sie können Sie auch verwenden, um Metadateninformationen über den Anbieter, seine Ereignisse und die Kanäle zu erhalten, in denen Ereignisse protokolliert werden, und um Ereignisse aus einer Kanal-oder Protokolldatei abzufragen. Das WevtUtil.exe Tool ist in% windir% \\ system32 enthalten. Geben Sie "wevtutil/?" ein, um Nutzungsinformationen zu erhalten. an einer Eingabeaufforderung.<br/> Dieser Befehl ist auf Mitglieder der Gruppe "Administratoren" beschränkt und muss mit erhöhten Rechten ausgeführt werden.|
