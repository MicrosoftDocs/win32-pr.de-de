---
title: Objekt Bezeichner (SNMP)
description: Ein SNMP-Objekt Bezeichner benennt ein Objekt eindeutig und identifiziert seinen Speicherort innerhalb einer MIB-Struktur (Management Information Base).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739329"
---
# <a name="object-identifiers-snmp"></a>Objekt Bezeichner (SNMP)

Ein SNMP-Objekt Bezeichner benennt ein Objekt eindeutig und identifiziert seinen Speicherort innerhalb einer MIB-Struktur (Management Information Base). Objekt Bezeichner sind Anwendungs unabhängige abstrakte Syntax Notation One (ASN. 1)-Datentypen, die aus einer Sequenz von nicht negativen ganzen Zahlen oder unter Elementen bestehen. Objekt Bezeichner müssen mindestens zwei untergeordnete IDs aufweisen, und Sie dürfen 128 subIdentifier nicht überschreiten.

Die WinSNMP-Programmierumgebung verwendet die [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur zum Verwalten von Objekt Bezeichners. Das Format des objektbezeichnerarrays in einer **smioid** -Struktur ist ein subIdentifier pro Array-Element.

Die Darstellung eines Objekt Bezeichners mit punktierter numerischer Zeichenfolge trennt seine unter Elemente in Zeiträume. Beispiel: "1.2.3.4.5.6".

Weitere Informationen finden Sie in [der SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) und in den entsprechenden RFCs.

 

 




