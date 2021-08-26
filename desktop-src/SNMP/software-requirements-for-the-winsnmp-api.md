---
title: Softwareanforderungen für die WinSNMP-API
description: Eine WinSNMP-Anwendung muss über die Dynamic Link Library-Api auf die WinSNMP-API WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886070"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Softwareanforderungen für die WinSNMP-API

Eine WinSNMP-Anwendung muss über die Dynamic Link Library-Api auf die WinSNMP-API WSNMP32.DLL.

Die folgenden Dateien sind erforderlich, um die Funktionalität der WinSNMP-API zu unterstützen.



| Dateiname     | BESCHREIBUNG                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. Lib  | WinSNMP-Bibliothek                                                                              |
| WSNMP32.DLL  | Stellt eine WinSNMP-Schnittstelle bereit.                                                                   |
| WINSNMP. H    | WinSNMP-Headerdatei                                                                          |
| SNMPTRAP.EXE | Empfängt SNMP-Traps und gibt sie an MGMTAPI.DLL, die Microsoft SNMP-Manager-API-Bibliothek, weiter. |
| SNMPAPI.DLL  | Stellt SNMP-Hilfsprogramme zur                                                                      |



 

 

 




