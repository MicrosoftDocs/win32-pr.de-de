---
title: Gesamtstrukturen
description: Eine Gesamtstruktur besteht aus einer oder mehr Domänenstrukturen, die keinen zusammenhängenden Namespace bilden.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- Active Directory-Gesamtstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ccccbce1c660c3f1e185e75971aa71d613c2db012ce42979cfaee7cd9c2b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189204"
---
# <a name="forests"></a>Gesamtstrukturen

Eine [*Gesamtstruktur*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) besteht aus einer oder mehr Domänenstrukturen, die keinen zusammenhängenden Namespace bilden. Alle Strukturen in einer Gesamtstruktur verwenden ein gemeinsames Schema, eine Konfiguration und einen globalen Katalog. Alle Strukturen in einer bestimmten Gesamtstruktur tauschen die Vertrauensstellung gemäß transitiven hierarchischen Kerberos-Vertrauensstellungen aus. Im Gegensatz zu Strukturen erfordert eine Gesamtstruktur keinen eindeutigen Namen. Eine Gesamtstruktur ist als Satz von Querverweisobjekten und Kerberos-Vertrauensstellungen vorhanden, die von den Memberstrukturen erkannt werden. Strukturen in einer Gesamtstruktur bilden eine Hierarchie für die Zwecke der Kerberos-Vertrauensstellung. Der Strukturname im Stammverzeichnis der Vertrauensstruktur verweist auf eine bestimmte Gesamtstruktur.

Die folgende Abbildung zeigt eine Gesamtstruktur nicht zusammenhängender Namespaces.

![Gesamtstruktur nicht zusammenhängender Namespaces](images/forests.png)

 

 