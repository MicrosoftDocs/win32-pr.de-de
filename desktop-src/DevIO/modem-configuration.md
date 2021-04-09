---
description: Mit Modem Konfigurationsfunktionen können Sie ein Modem konfigurieren, bevor Sie eine Verbindung herstellen.
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: Modem Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861476"
---
# <a name="modem-configuration"></a>Modem Konfiguration

Mit Modem Konfigurationsfunktionen können Sie ein Modem konfigurieren, bevor Sie eine Verbindung herstellen. Eine Anwendung kann Modem Optionen festlegen und die Features eines Modem ermitteln, ohne dass für Modem gerätespezifische Befehle verwendet werden. Im folgenden finden Sie die allgemeinen Features, die eine Anwendung vor dem Ausführen eines Aufrufes festlegen kann

-   Primärer Betriebsmodus (synchron, asynchron und gibt an, ob die Fehler Steuerung aktiviert ist).
-   V. 42 Error Control (definiert durch die CCITT-Empfehlung V. 42), einschließlich spezifischer Parameter. CCITT steht für den internationalen telefonischen und Telefon Beratungsausschuss.
-   V. 42 bis (definiert durch die CCITT-Empfehlung V. 42 bis) und die MNP5-Datenkomprimierung.
-   Timeout Optionen, einschließlich Setup für Anrufe, Inaktivität und gepufferte Datenübermittlung.

Vor dem Festlegen der Konfiguration eines Modem sollte eine Anwendung die Funktionen des Modem Geräts mithilfe der [**getcommproperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) -Funktion bestimmen. Diese Funktion füllt eine [**commprop**](/windows/desktop/api/WinBase/ns-winbase-commprop) -Struktur aus. Diese Struktur enthält sowohl einen allgemeinen Teil, der für alle Kommunikationsgeräte gilt, als auch einen Teil, der für jeden Anbieter Untertyp spezifisch ist. Bei Modem Geräten ist der anbieterspezifische Teil der **commprop** -Struktur eine [**modemdevcaps**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) -Struktur.

Eine Anwendung kann die aktuelle Konfiguration eines Modem mithilfe der Funktionen [**getcommconfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) und [**setcommconfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) aufrufen und festlegen, von denen beide eine [**CommConfig**](/windows/desktop/api/Winbase/ns-winbase-commconfig) -Struktur verwenden. Diese Struktur enthält sowohl einen allgemeinen Teil, der für alle Kommunikationsgeräte gilt, als auch einen Teil, der für jeden Anbieter Untertyp spezifisch ist. Bei Modem Geräten ist der anbieterspezifische Teil der **CommConfig** -Struktur eine [**modemsettings**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) -Struktur.

Nach dem Konfigurieren eines Modem kann eine Anwendung die Telefonie-Anwendungsprogrammierschnittstelle verwenden, um tatsächlich eine Verbindung herzustellen.

Die Modem Konfigurationsfunktionen bieten keine langfristige Verwaltung und Wartung eines Modem. Modem Dienstanbieter sollten zu diesem Zweck Modem Konfigurations Dialogfelder bereitstellen.

 

 



