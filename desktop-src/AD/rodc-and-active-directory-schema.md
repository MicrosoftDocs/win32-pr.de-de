---
title: Read-Only DCS und das Active Directory Schema
description: Windows Server 2008 führt eine neue Art von Domänen Controller ein, den schreibgeschützten Domänen Controller (Read-Only Domain Controller, RODC).
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102495"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only DCS und das Active Directory Schema

Windows Server 2008 führt eine neue Art von Domänen Controller ein, den schreibgeschützten Domänen Controller (Read-Only Domain Controller, RODC). Dadurch wird ein Domänen Controller für die Verwendung in Zweigniederlassungen bereitgestellt, in denen kein vollständiger Domänen Controller platziert werden kann. Die Absicht besteht darin, Benutzern in den Zweigstellen zu gestatten, sich zu anmelden und Aufgaben wie die Datei-/Druckerfreigabe auszuführen, auch wenn keine Netzwerk Konnektivität mit Hub-Standorten vorhanden ist.

RODC ändert nicht die Art und Weise, in der das Schema verwendet wird. Es lohnt sich jedoch zu erwähnen, dass das Schema einen Read-Only partiellen Attribut Satz (sspas) unterstützt, der auch als RODC-gefilterter Attribut Satz bezeichnet wird. Hierbei handelt es sich um einen speziellen Attribut Satz, der aus Sicherheitsgründen nicht in RODCs repliziert wird. RO-pas werden im Schema über das [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut definiert.

## <a name="rodc-filtered-attribute-set"></a>Gefilterter RODC-Attribut Satz

Einige Anwendungen, die [Active Directory Domain Services](active-directory-domain-services.md) als Datenspeicher verwenden, verfügen möglicherweise über Anmelde Informations ähnliche Daten (z. b. Kenn Wörter, Anmelde Informationen oder Verschlüsselungsschlüssel), die nicht auf einem Read-Only Domänen Controller gespeichert werden sollen, falls der RODC gestohlen oder kompromittiert wird. Für diesen Anwendungstyp können Sie das-Attribut zum gefilterten RODC-Attribut hinzufügen, um zu verhindern, dass es in RODCs in der Gesamtstruktur repliziert wird, und das Attribut als vertraulich markieren, wodurch die Fähigkeit zum Lesen der Daten für Mitglieder der Gruppe "authentifizierte Benutzer" (einschließlich aller RODCs) entfällt.

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>Hinzufügen von Attributen zum gefilterten RODC-Attribut Satz

Der gefilterte RODC-Attribut Satz ist ein dynamischer Satz von Attributen, der nicht auf RODCs in der Gesamtstruktur repliziert wird. Sie können den gefilterten RODC-Attribut Satz für einen Schema Master konfigurieren, auf dem Windows Server 2008 ausgeführt wird. Wenn die Attribute an der Replikation in RODCs gehindert werden, können diese Daten nicht unnötig verfügbar gemacht werden, wenn ein RODC gestohlen oder kompromittiert wird.

Sie können dem RODC-gefilterten Attribut Satz keine systemkritischen Attribute hinzufügen. Ein Attribut ist System kritisch, wenn es für AD DS, lokale Sicherheits Autorität (Local Security Authority, LSA), Sicherheits Konten Verwaltung (Security Accounts Manager, Sam) und einen Microsoft-spezifischen Sicherheits Dienstanbieter (z. b. das Kerberos-Authentifizierungsprotokoll) erforderlich ist, um ordnungsgemäß zu funktionieren. In Versionen von Windows Server 2008 nach Beta 3 weist ein System kritisches Attribut den Wert des schemaFlagsEx-Attributs auf (schemaFlagsEx-Attribut Wert & 0x1 = **true**).

Schritt-für-Schritt-Anweisungen zum Hinzufügen von Attributen zum gefilterten RODC-Attribut Satz finden Sie in [Anhang D der Schritt-für-Schritt-Anleitung für RODCs]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10)).

## <a name="marking-attributes-as-confidential"></a>Markieren von Attributen als vertraulich

Außerdem wird empfohlen, dass Sie auch alle Attribute als vertraulich markieren, die Sie als Teil des gefilterten RODC-Attribut Satzes konfigurieren. Zum Markieren eines vertraulichen Attributs müssen Sie die Berechtigung Lesen für das Attribut für die Gruppe Authentifizierte Benutzer entfernen. Das Markieren des Attributs als vertraulich bietet einen zusätzlichen Schutz gegen einen RODC, der kompromittiert wird, indem die Berechtigungen entfernt werden, die zum Lesen der Daten mit Anmelde Informationen benötigt werden. Weitere Informationen zum Markieren von Attributen als vertraulich finden Sie [im Artikel 922836 in der Microsoft Knowledge Base]( https://support.microsoft.com/kb/922836).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt-für-Schritt-Anleitung für schreibgeschützte Domänen Controller]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 