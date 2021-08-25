---
description: Eine Sicherheitsbeschreibung enthält die Sicherheitsinformationen, die einem sicherungsfähigen Objekt zugeordnet sind.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Sicherheitsbeschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1049becf755bbb0940cfd5def3b59662a20eb2a690d90a36e06c5706212f02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907190"
---
# <a name="security-descriptors"></a>Sicherheitsbeschreibungen

Eine [*Sicherheitsbeschreibung*](/windows/desktop/SecGloss/s-gly) enthält die Sicherheitsinformationen, die einem [sicherungsfähigen Objekt](securable-objects.md)zugeordnet sind. Eine Sicherheitsbeschreibung besteht aus einer [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) und den zugehörigen Sicherheitsinformationen. Eine Sicherheitsbeschreibung kann die folgenden Sicherheitsinformationen enthalten:

-   [Sicherheitsbezeichner](security-identifiers.md) (SIDs) für den Besitzer und die primäre Gruppe eines Objekts.
-   Eine [DACL,](access-control-lists.md) die die Zugriffsrechte angibt, die bestimmten Benutzern oder Gruppen gewährt oder verweigert werden.
-   Eine [SACL,](access-control-lists.md) die die Typen von Zugriffsversuchen angibt, die Überwachungsdatensätze für das Objekt generieren.
-   Eine Reihe von Steuerelementbits, die die Bedeutung eines Sicherheitsdeskriptors oder seiner einzelnen Member qualifizieren.

Anwendungen dürfen den Inhalt einer Sicherheitsbeschreibung nicht direkt bearbeiten. Die Windows-API stellt Funktionen zum Festlegen und Abrufen der Sicherheitsinformationen in der Sicherheitsbeschreibung eines Objekts bereit. Darüber hinaus gibt es Funktionen zum Erstellen und Initialisieren eines Sicherheitsdeskriptors für ein neues -Objekt.

Anwendungen, die mit Sicherheitsbeschreibungen für Active Directory-Objekte arbeiten, können die Windows Sicherheitsfunktionen oder die sicherheitsschnittstellen verwenden, die von den Active Directory-Dienstschnittstellen (ADSI) bereitgestellt werden. Weitere Informationen zu ADSI-Sicherheitsschnittstellen finden Sie unter [Funktionsweise von Access Control in Active Directory.](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services)

 

 
