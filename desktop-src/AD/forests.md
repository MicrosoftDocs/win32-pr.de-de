---
title: Gesamtstrukturen
description: Eine Gesamtstruktur ist ein Satz von mindestens einer Domänen Struktur, die keinen zusammenhängenden Namespace bilden.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- Gesamtstruktur Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948570"
---
# <a name="forests"></a>Gesamtstrukturen

Eine Gesamt [*Struktur ist ein*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) Satz von mindestens einer Domänen Struktur, die keinen zusammenhängenden Namespace bilden. Alle Strukturen in einer Gesamtstruktur verfügen über ein gemeinsames Schema, eine gemeinsame Konfiguration und einen globalen Katalog. Alle Strukturen in einer bestimmten Gesamtstruktur tauschen eine Vertrauensstellung gemäß transitiven hierarchischen Kerberos-Vertrauens Stellungen aus. Im Gegensatz zu Strukturen ist für eine Gesamtstruktur kein eindeutiger Name erforderlich. Eine Gesamtstruktur ist als Satz von Querverweis Objekten und Kerberos-Vertrauens Stellungen vorhanden, die von den Mitglieds Strukturen erkannt werden. Strukturen in einer Gesamtstruktur bilden eine Hierarchie für die Kerberos-Vertrauensstellung. der Struktur Name im Stammverzeichnis der Vertrauens Struktur verweist auf eine angegebene Gesamtstruktur.

Die folgende Abbildung zeigt eine Gesamtstruktur von nicht zusammenhängenden Namespaces.

![Gesamtstruktur von nicht zusammenhängenden Namespaces](images/forests.png)

 

 