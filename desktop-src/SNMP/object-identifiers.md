---
title: Objektbezeichner (SNMP)
description: Ein SNMP-Objektbezeichner benennt ein Objekt eindeutig und identifiziert seine Position innerhalb einer MIB-Struktur (Management Information Base).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81d52e43cb3be89551dd597bc5084d533f3913264f8bcf5c0a2ef7dbb375bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009258"
---
# <a name="object-identifiers-snmp"></a>Objektbezeichner (SNMP)

Ein SNMP-Objektbezeichner benennt ein Objekt eindeutig und identifiziert seine Position innerhalb einer MIB-Struktur (Management Information Base). Objektbezeichner sind anwendungsunabhängige ASN.1-Datentypen (Abstract Syntax Notation One), die aus einer Sequenz von nicht negativen ganzen Zahlen oder Untergeordneten Bezeichnern bestehen. Objektbezeichner müssen mindestens zwei Unteridentifizierer haben und dürfen 128 Unteridentifizierer nicht überschreiten.

Die WinSNMP-Programmierumgebung verwendet die [**smiOID-Struktur,**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) um Objektbezeichner zu verwalten. Das Format des Objektbezeichnerarrays in einer **smiOID-Struktur** ist ein Unteridentifizierer pro Arrayelement.

Die gepunktete numerische Zeichenfolgendarstellung eines Objektbezeichners trennt seine Unteridentifizierer durch Punkte. Beispiel: "1.2.3.4.5.6".

Weitere Informationen finden Sie unter [The SNMP Management Information Base (MIB) und](the-snmp-management-information-base-mib-.md) die relevanten RFCs.

 

 




