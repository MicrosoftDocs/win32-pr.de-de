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
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="422bf-103">Profil-und Konfigurations Einrichtung im eingeschränkten Modus</span><span class="sxs-lookup"><span data-stu-id="422bf-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="422bf-104">Aufgrund der Vielzahl von Datentypen, die von DirectX VA decodiert werden können, und die Konfigurationen mit mehreren decodierungen, die in DirectX VA für die einzelnen Datentypen unterstützt werden (z. b. die Verwendung von bitstreampuffern im Vergleich zum Decodieren von Host-Rest-unterschieden im Vergleich zu Accelerator-basierten IDCT mit und ohne Verschlüsselung jedes relevanten Puffer Typs usw</span><span class="sxs-lookup"><span data-stu-id="422bf-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="422bf-105">Dadurch wird eine große Anzahl von GUIDs erstellt (z. b. hypothetisch, wenn es 16 Profile mit DirectX VA und 16 Konfigurationen gibt), müssten 256 definierte GUIDs vorhanden sein – und Sie benötigen 4 KB an Arbeitsspeicher, um alle Dateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="422bf-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="422bf-106">Dieses Problem ist der schwierigste Aspekt bei der Bestimmung, wie DirectX VA in **iamvideoaccelerator** zugeordnet werden soll, wobei die restliche Betriebs Definition größtenteils recht unkompliziert ist.</span><span class="sxs-lookup"><span data-stu-id="422bf-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="422bf-107">Daher geben wir eine eindeutige GUID für jeden Datentyp an (für jedes Profil mit eingeschränktem Modus) und ermöglichen es, jeder Art von Verschlüsselung eine weitere GUID zugeordnet zu werden.</span><span class="sxs-lookup"><span data-stu-id="422bf-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="422bf-108">Die Decodierungs Konfiguration wird dann zwischen dem Decoder und dem Accelerator durch eine untergeordnete Aushandlungs Verhandlung mithilfe von Prüf-und Sperr Vorgängen eingerichtet, um Konfigurationen für jeden Typ der DirectX-VA-Funktion einzurichten.</span><span class="sxs-lookup"><span data-stu-id="422bf-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



