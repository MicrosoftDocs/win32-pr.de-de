---
description: Profil-und Konfigurations Einrichtung im eingeschränkten Modus
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Profil-und Konfigurations Einrichtung im eingeschränkten Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392533"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Profil-und Konfigurations Einrichtung im eingeschränkten Modus

Aufgrund der Vielzahl von Datentypen, die von DirectX VA decodiert werden können, und die Konfigurationen mit mehreren decodierungen, die in DirectX VA für die einzelnen Datentypen unterstützt werden (z. b. die Verwendung von bitstreampuffern im Vergleich zum Decodieren von Host-Rest-unterschieden im Vergleich zu Accelerator-basierten IDCT mit und ohne Verschlüsselung jedes relevanten Puffer Typs usw Dadurch wird eine große Anzahl von GUIDs erstellt (z. b. hypothetisch, wenn es 16 Profile mit DirectX VA und 16 Konfigurationen gibt), müssten 256 definierte GUIDs vorhanden sein – und Sie benötigen 4 KB an Arbeitsspeicher, um alle Dateien zu speichern. Dieses Problem ist der schwierigste Aspekt bei der Bestimmung, wie DirectX VA in **iamvideoaccelerator** zugeordnet werden soll, wobei die restliche Betriebs Definition größtenteils recht unkompliziert ist. Daher geben wir eine eindeutige GUID für jeden Datentyp an (für jedes Profil mit eingeschränktem Modus) und ermöglichen es, jeder Art von Verschlüsselung eine weitere GUID zugeordnet zu werden. Die Decodierungs Konfiguration wird dann zwischen dem Decoder und dem Accelerator durch eine untergeordnete Aushandlungs Verhandlung mithilfe von Prüf-und Sperr Vorgängen eingerichtet, um Konfigurationen für jeden Typ der DirectX-VA-Funktion einzurichten.

 

 



