---
title: Steuern des Zugriffs auf Objekte und deren Eigenschaften
description: Um den Zugriff auf Anwendungs Objekte zu steuern, arbeiten Sie mit der Objekt Sicherheits Beschreibung und insbesondere mit der freigegebenen Zugriffs Steuerungs Liste (DACL) und der Liste der Zugriffs Steuerungs Einträge (ACEs).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- Objekt-AD, Steuern des Zugriffs auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206213"
---
# <a name="controlling-access-to-objects-and-their-properties"></a>Steuern des Zugriffs auf Objekte und deren Eigenschaften

Um den Zugriff auf Anwendungs Objekte zu steuern, arbeiten Sie mit der Objekt Sicherheits Beschreibung und insbesondere mit der freigegebenen Zugriffs Steuerungs Liste (DACL) und der Liste der Zugriffs Steuerungs Einträge (ACEs).

Wenn ein Objekt erstellt wird, empfängt es eine Sicherheits Beschreibung. Weitere Informationen und eine Beschreibung der Regeln, die das System verwendet, um die DACL für ein neues Objekt zu erstellen, finden Sie unter [Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte](how-security-descriptors-are-set-on-new-directory-objects.md). Diese Regeln zeigen, dass Sie folgende Aktionen ausführen können:

-   Erstellen Sie eine neue Sicherheits Beschreibung, und fügen Sie Sie zum Zeitpunkt der Erstellung an das Objekt an. Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Verzeichnis Objekt](creating-a-security-descriptor-for-a-new-directory-object.md).
-   Anwenden eines vererbbaren ACE an einem beliebigen Punkt in der Verzeichnishierarchie, sodass ein ACE von Objekten in der Struktur geerbt wird. Ein Objekt kann einen ACE von seinem übergeordneten Container erben. Weitere Informationen finden Sie unter [Vererbung und Delegierung der Verwaltung](inheritance-and-delegation-of-administration.md).
-   Geben Sie einen ACE in der standarddacl im Schema an, wenn Sie über die erforderlichen Zugriffsrechte verfügen. Jede Objektklassen Definition im Schema enthält eine Standard Sicherheits Beschreibung, die über eine standardmäßige DACL verfügen kann. Weitere Informationen finden Sie unter [Standard Sicherheits Beschreibung](default-security-descriptor.md).

Außerdem kann die DACL eines vorhandenen Objekts geändert werden. Ihre Möglichkeiten:

-   Ersetzen Sie die DACL durch eine neue.
-   Lesen Sie die vorhandene DACL, ändern Sie Sie, und wenden Sie die geänderte DACL an. Weitere Informationen finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).

In der folgenden Liste wird die wichtigste Funktion eines ACE in Active Directory Domain Services beschrieben. Mit einem ACE haben Sie folgende Möglichkeiten:

-   Steuern, wer bestimmte Vorgänge für ein Objekt ausführen kann.
-   Steuern, wer Zugriff auf eine bestimmte Eigenschaft oder einen Satz von Eigenschaften für ein Objekt hat.
-   Steuern, wer untergeordnete Objekte in einem Container erstellen kann, einschließlich der Person, die einen bestimmten Typ von untergeordnetem Objekt erstellen kann.
-   Definieren privater Zugriffsrechte für einen Objekttyp und Steuern, wer die durch die privaten Rechte geschützten Vorgänge ausführen kann.
-   Wenden Sie einen ACE auf ein Container Objekt am Stamm einer Verzeichnis Unterstruktur an, sodass der Schutz von allen untergeordneten Objekten in der Struktur automatisch geerbt werden kann.
-   Anwenden eines ACE, der automatisch von einem bestimmten Typ eines untergeordneten Objekts in einer Unterstruktur geerbt wird.
-   Erstellen Sie einen ACE, der der Sicherheitsgruppe Rechte erteilt, nicht einem einzelnen Benutzer.
-   Wenden Sie einen ACE auf Gruppenrichtlinie Objekte an, um die von der Richtlinie betroffenen Konten und Computer zu steuern.

 

 




