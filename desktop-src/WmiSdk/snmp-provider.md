---
description: Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über Windows-Verwaltungsinstrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI und SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218489"
---
# <a name="wmi-and-snmp"></a>WMI und SNMP

Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über Windows-Verwaltungsinstrumentation (WMI). Der SNMP-Anbieter ist standardmäßig nicht installiert. Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

SNMP (Simple Network Management Protocol) verwendet ein Schema zum Definieren von Objekten. Das Schema unterscheidet sich von dem in WMI verwendeten Schema. Das Schema SNMPv1 und SNMPv2C wird als Struktur von Verwaltungsinformationen (SMI) bezeichnet und als MIB-Dateien (Management Information Base) verpackt. MIB-Dateien definieren Objekte mithilfe einer Standardsprache – Abstract Syntax Notation 1 (ASN. 1) – und einer Reihe von Makro Definitionen, die als Vorlagen zum Beschreiben der Objekte dienen. Die Makros stellen Informationen wie den Objektnamen, den Bezeichner, die Syntax, die Beschreibung, Zugriffsrechte, Protokoll Vorgänge und die Protokoll Codierung bereit. In der folgenden Tabelle ist aufgelistet, wie der SNMP-Anbieter verschiedene Aspekte eines MIB-Objekts behandelt.



| Thema                                                    | BESCHREIBUNG                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [Notification-Type-Makro](notification-type-macro.md)   | Gibt an, wie das **-Benachrichtigungstyp-** Makro von SNMP zu WMI zugeordnet wird.  |
| [Object-Type-Makro](object-type-macro.md)               | Gibt an, wie das **Objekttyp-** Makro von SNMP zu WMI zugeordnet wird.        |
| [Text Konvention-Makro](textual-convention-macro.md) | Gibt an, wie das **Textkonventionen-** Makro von SNMP zu WMI zugeordnet wird. |
| [Trap-Type-Makro](trap-type-macro.md)                   | Gibt an, wie das **Trap-Type-** Makro von SNMP zu WMI zugeordnet wird.          |



 

Der SNMP-Anbieter enthält einen Compiler, der MIB-Objekte in WMI-Objekte übersetzt. Der SNMP-Compiler kann auch Fehler oder andere Nachrichten ausgeben. Weitere Informationen finden Sie unter [SNMP-Compilerfehlermeldungen](snmp-compiler-error-messages.md) und [Allgemeine Informationsmeldungen](general-information-messages.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> </dl>

 

 



