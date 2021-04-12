---
title: Software Anforderungen für die WinSNMP-API
description: Eine WinSNMP-Anwendung muss über die Dynamic Link Library-WSNMP32.DLL auf die WinSNMP-API zugreifen.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206232"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Software Anforderungen für die WinSNMP-API

Eine WinSNMP-Anwendung muss über die Dynamic Link Library-WSNMP32.DLL auf die WinSNMP-API zugreifen.

Die folgenden Dateien sind erforderlich, um die Funktionalität der WinSNMP-API zu unterstützen.



| Dateiname     | BESCHREIBUNG                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. LIB  | WinSNMP-Bibliothek                                                                              |
| WSNMP32.DLL  | Stellt WinSNMP-Schnittstelle bereit                                                                   |
| Winsnmp. Micha    | WinSNMP-Header Datei                                                                          |
| SNMPTRAP.EXE | Empfängt SNMP-Traps und leitet Sie an MGMTAPI.DLL, die Microsoft SNMP Manager-API-Bibliothek. |
| SNMPAPI.DLL  | Stellt SNMP-Hilfsprogramme bereit                                                                      |



 

 

 




