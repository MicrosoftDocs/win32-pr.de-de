---
description: Das Installieren einer Monitor-dll ist ein einfacher Prozess.
ms.assetid: f2c18faa-0010-4d26-b7e9-e8a7b5d11981
title: Installieren eines Monitors zum Netzwerkmonitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7fb6847d1ea93895b190ce2377247c586c06f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218844"
---
# <a name="installing-a-monitor-to-network-monitor"></a>Installieren eines Monitors zum Netzwerkmonitor

Das Installieren einer Monitor-dll ist ein einfacher Prozess. Kopieren Sie zunächst die dll und das zugehörige HTML-Konfigurations Formular in das Unterverzeichnis Ihrer NPP-Monitore (z \\ . b. C: Windows \\ system32 \\ NPP- \\ Monitore). Beim Kopieren in das Verzeichnis wird der Monitor erkannt und ist verfügbar, wenn das Überwachungs Steuerungs Tool oder der Überwachungs Steuerungs Dienst (Monitor Control Service, mcsvc) das nächste Mal aktiviert wird.

Wenn die Umgebungsvariable "% SystemRoot%" beispielsweise "c: \\ Windows" ist, ist das Monitor-Unterverzeichnis "c: \\ Windows \\ system32 \\ NPP \\ Monitors".

 

 



