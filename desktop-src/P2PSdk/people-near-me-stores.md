---
description: Personen in meiner Umgebung speichern
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Personen in meiner Umgebung speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866695"
---
# <a name="people-near-me-stores"></a>Personen in meiner Umgebung speichern

Anwendungen, die [Personen in meiner](about-people-near-me.md) Umgebung (PNM) unterstützen, können die folgenden Datenspeicher verwenden:

### <a name="windows-address-book"></a>Windows-Adressbuch

Das Windows-Adressbuch speichert Informationen zu Kontakten und Ihren digitalen Zertifikaten. Der Kontakt "**Me**", der den derzeit angemeldeten Benutzer darstellt, wird ebenfalls im Windows-Adressbuch gespeichert.

### <a name="certificate-store"></a>Zertifikatspeicher

Der Zertifikat Speicher enthält das selbst signierte Zertifikat für den "**Me**"-Kontakt.

### <a name="application-store"></a>Anwendungsstore

Ein Anwendungsinstallations Programm registriert eine Anwendung bei PNM während des Installationsvorgangs. Dabei handelt es sich um Objekte, die von anderen Benutzern durchsucht werden können, wenn versucht wird, eine Verbindung mit einem Benutzer mit einer allgemeinen Anwendung herzustellen, z. b. einem Computerspiel. Der Anwendungs Speicher enthält für jede Anwendung den Namen der Anwendung, eine Globally Unique Identifier (GUID), einen Bereich der Anwendung, eine Beschreibung und einen Pfad zur ausführbaren Datei des Programms. Der Geltungsbereich einer Anwendung kann auf keine (nicht angekündigt), Personen in der Nähe (angekündigt im lokalen Subnetz), Kontakte (angekündigt nur für Kontakte) oder alle (angekündigt im lokalen Subnetz und für Kontakte) festgelegt werden. Der Anwendungs Speicher befindet sich in der Windows Vista-Registrierung.

 

 



