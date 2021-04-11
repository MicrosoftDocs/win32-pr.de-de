---
description: NLS umfasst eine Reihe von API-Funktionen, die Ihre Anwendungen verwenden können, um Gebiets Schema Daten zwischen Gebiets Schema Bezeichners und Gebiets Schema Namen zuzuordnen und neutrale Gebiets Schemas aufzulisten.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Zuordnung von Gebiets Schema Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214958"
---
# <a name="mapping-locale-data"></a>Zuordnung von Gebiets Schema Daten

NLS umfasst eine Reihe von API-Funktionen, die Ihre Anwendungen verwenden können, um Gebiets Schema Daten zwischen Gebiets Schema Bezeichners und Gebiets Schema [Namen](locale-names.md) [zuzuordnen und neutrale](locale-identifiers.md) Gebiets Schemas aufzulisten. In diesem Thema wird die Verwendung dieser Funktionen unter Windows Vista und höher und unter Windows Vista-Betriebssystemen (manchmal auch als "downlevelsysteme" bezeichnet) erörtert.

## <a name="map-locale-data-on-windows-vista-and-later"></a>Zuordnen von Gebiets Schema Daten unter Windows Vista und höher

NLS bietet verschiedene Funktionen für die Gebiets Schema Zuordnung, die von Anwendungen verwendet werden können, die Sie für die unter Windows Vista und höher entwickeln. Sie enthält auch Funktionen, die Ihre Anwendungen verwenden können, um neutrale Gebiets Schemas aufzuzählen.

**Verwenden der Standard Konvertierungs Funktionen für die Datenzuordnung**

Um zwischen einem Gebiets Schema Namen und einem Gebiets Schema Bezeichner zuzuordnen, kann die Anwendung die [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) -Funktion abrufen. Die Anwendung verwendet [**lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) , um eine Zuordnung zwischen einem Gebiets Schema Bezeichner und einem Gebiets Schema Namen zu verwenden.

**Auflisten neutraler Gebiets Schemas**

Um neutrale Gebiets Schemata für Windows 7 und höher aufzulisten, kann die Anwendung [**enumsystemlocalesex**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) mit *dwFlags* aufrufen, die auf [**locale \_ neutraldata**](locale-neutraldata.md)festgelegt sind. Außerdem kann [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) verwendet werden, wobei *LCTYPE* auf [**locale \_ ineutral**](locale-ineutral.md)festgelegt ist.

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Zuordnen von Gebiets Schema Daten auf Betriebssystemen vor Windows Vista

NLS enthält eine Direct Link Library (dll) zur Verwendung für Anwendungen, die Sie für die Betriebssysteme vor Windows Vista entwickeln. Die DLL unterstützt sowohl Konvertierungs-als auch Listen Funktionen für die Datenzuordnung.

> [!Note]  
> Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten nicht die downlevelzuordnung oder die Auflistungs Funktionen verwenden.

 

**Verwenden der Downlevel-Konvertierungs Funktionen für die Datenzuordnung**

Ihre Anwendung, die auf ein downlevelsystem ausgerichtet ist, kann die [**downlevellcidtolocalename**](downlevellcidtolocalename.md) -Funktion zum Konvertieren eines Gebiets Schema Bezeichners in einen Gebiets Schema Namen abrufen. Wenn ein Gebiets Schema Name in einen Gebiets Schema Bezeichner konvertiert werden muss, sollte er [**downlevellocalenametolcid**](downlevellocalenametolcid.md)nennen.

**Verwenden der Funktionen für die downlevelauflistung zum Auflisten neutraler Gebiets Schemas**

Die Anwendung sollte die [**downlevelgetparametrilocalelcid**](downlevelgetparentlocalelcid.md) aufrufen, um den Gebiets Schema Bezeichner des übergeordneten Elements für ein Gebiets Schema abzurufen. Wenn die Anwendung den Gebiets Schema Namen des übergeordneten Elements für das Gebiets Schema abrufen muss, sollte Sie [**downlevelgetparametrilocalename**](downlevelgetparentlocalename.md)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> <dt>

[Gebiets Schema Bezeichner](locale-identifiers.md)
</dt> <dt>

[Gebiets Schema Namen](locale-names.md)
</dt> </dl>

 

 



