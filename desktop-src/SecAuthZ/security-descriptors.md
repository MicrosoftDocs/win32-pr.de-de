---
description: Eine Sicherheits Beschreibung enthält die Sicherheitsinformationen, die einem Sicherungs fähigen Objekt zugeordnet sind.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Sicherheitsbeschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863007"
---
# <a name="security-descriptors"></a>Sicherheitsbeschreibungen

Eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) enthält die Sicherheitsinformationen, die einem Sicherungs [fähigen Objekt](securable-objects.md)zugeordnet sind. Eine Sicherheits Beschreibung besteht aus einer [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) und den zugehörigen Sicherheitsinformationen. Eine Sicherheits Beschreibung kann die folgenden Sicherheitsinformationen enthalten:

-   [Sicherheits](security-identifiers.md) -IDs (SIDs) für den Besitzer und die primäre Gruppe eines Objekts.
-   Eine [DACL](access-control-lists.md) , die die Zugriffsrechte angibt, die bestimmten Benutzern oder Gruppen gewährt oder verweigert werden.
-   Eine [SACL](access-control-lists.md) , die die Typen von Zugriffsversuchen angibt, die Überwachungsdaten Sätze für das Objekt generieren.
-   Ein Satz von Steuerungs Bits, die die Bedeutung einer Sicherheits Beschreibung oder ihrer einzelnen Member qualifizieren.

Anwendungen dürfen den Inhalt einer Sicherheits Beschreibung nicht direkt bearbeiten. Die Windows-API stellt Funktionen zum Festlegen und Abrufen der Sicherheitsinformationen in der Sicherheits Beschreibung eines Objekts bereit. Außerdem gibt es Funktionen zum Erstellen und Initialisieren einer Sicherheits Beschreibung für ein neues-Objekt.

Anwendungen, die mit Sicherheits Deskriptoren auf Active Directory Objekten arbeiten, können die Windows-Sicherheitsfunktionen oder die von den Active Directory Service Interfaces (ADSI) bereitgestellten Sicherheits Schnittstellen verwenden. Weitere Informationen zu ADSI-Sicherheits Schnittstellen finden Sie unter [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
