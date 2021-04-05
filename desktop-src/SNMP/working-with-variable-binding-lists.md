---
title: Arbeiten mit Variablen Bindungs Listen
description: Eine Variablen Bindung ist die Kopplung eines SNMP-objektinstanznamens mit einem zugeordneten Wert. Eine Variablen Bindungs Liste ist eine Reihe von Variablen Bindungs Einträgen. In WinSNMP enthält eine Protokolldaten Einheit (PDU) eine Variablen Bindungs Liste.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Arbeiten mit Variablen Bindungs Listen SNMP
- Variablen Bindung listet SNMP, SNMP auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723664"
---
# <a name="working-with-variable-binding-lists"></a>Arbeiten mit Variablen Bindungs Listen

Eine *Variablen Bindung* ist die Kopplung eines SNMP-objektinstanznamens mit einem zugeordneten Wert. Eine *Variablen Bindungs Liste* ist eine Reihe von Variablen Bindungs Einträgen. In WinSNMP enthält eine Protokolldaten Einheit (PDU) eine Variablen Bindungs Liste.

Die Details der Variablen Bindungs Listenstruktur sind auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann auf eine Variablen Bindungs Liste mit einem Handle des Typs **hsnmp \_ VBL** zugreifen. Weitere Informationen finden Sie unter [Ressourcenhandle-Objekte](resource-handle-objects.md).

Die WinSNMP-Anwendung kann Variablen Bindungs Listen erstellen und bearbeiten und Sie in PDUs einschließen. Zum Ausführen dieser Vorgänge verwendet die Anwendung die WinSNMP- [Variablen Bindungsfunktionen](winsnmp-functions.md). Weitere Informationen zum Arbeiten mit WinSNMP und Variablen Bindungs Listen finden Sie in den in der folgenden Tabelle aufgeführten Themen.



| Thema                                                                    | BESCHREIBUNG                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [Erstellen einer Variablen Bindungs Liste](creating-a-variable-binding-list.md) | Beschreibt, wie eine Variablen Bindungs Liste erstellt wird. |
| [Verwalten einer Variablen Bindungs Liste](managing-a-variable-binding-list.md) | Beschreibt, wie eine Variablen Bindungs Liste verwaltet wird. |



 

Weitere Informationen zu Variablen Bindungen und Variablen Bindungs Listen finden Sie unter [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protokoll Vorgänge für Version 2 des Simple Network Management-Protokolls (SNMPv2)" und der WinSNMP- [Variablen Bindungsfunktionen](winsnmp-functions.md).

 

 




