---
description: Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Clientanwendungen den Zugriff auf SNMP-Informationen über Windows Management Instrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI und SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f1327afe2a86a1f56f40c0a93d904148ccaf1fd0547b6cb623d9eb420c2a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992300"
---
# <a name="wmi-and-snmp"></a>WMI und SNMP

Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Clientanwendungen den Zugriff auf SNMP-Informationen über Windows Management Instrumentation (WMI). Der SNMP-Anbieter ist standardmäßig nicht installiert. Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

Simple Network Management Protocol (SNMP) verwendet ein Schema zum Definieren von Objekten. Das Schema ist anders als das in WMI verwendete Schema. Das SNMPv1- und SNMPv2C-Schema wird als Structure of Management Information (SMI) bezeichnet und als MIB-Dateien (Management Information Base) gepackt. MIB-Dateien definieren Objekte mithilfe einer Standardsprache – Abstract Syntax Notation 1 (ASN.1) – und einer Reihe von Makrodefinitionen, die als Vorlagen zum Beschreiben der Objekte dienen. Die Makros stellen Informationen wie Objektname, Bezeichner, Syntax, Beschreibung, Zugriffsrechte, Protokollvorgänge und Protokollcodierung zur Verfügung. In der folgenden Tabelle wird aufgeführt, wie der SNMP-Anbieter verschiedene Aspekte eines MIB-Objekts behandelt.



| Thema                                                    | BESCHREIBUNG                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [NOTIFICATION-TYPE-Makro](notification-type-macro.md)   | Die Zuordnung **des NOTIFICATION-TYPE-Makros** von SNMP zu WMI.  |
| [OBJECT-TYPE-Makro](object-type-macro.md)               | Die Zuordnung **des OBJECT-TYPE-Makros** von SNMP zu WMI.        |
| [TEXTUAL-CONVENTION-Makro](textual-convention-macro.md) | Die Zuordnung **des TEXTUAL-CONVENTION-Makros** von SNMP zu WMI. |
| [TRAP-TYPE-Makro](trap-type-macro.md)                   | Die Zuordnung **des TRAP-TYPE-Makros** von SNMP zu WMI.          |



 

Der SNMP-Anbieter verfügt über einen Compiler, der MIB-Objekte in WMI-Objekte übersetzt. Der SNMP-Compiler kann auch Fehler oder andere Meldungen ausgegeben. Weitere Informationen finden Sie unter [Fehlermeldungen des SNMP-Compilers und](snmp-compiler-error-messages.md) [Allgemeine Informationsmeldungen.](general-information-messages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 



