---
title: Übersicht über die SSPI-Architektur
description: SSPI ist eine Softwareschnittstelle.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039336"
---
# <a name="sspi-architectural-overview"></a>Übersicht über die SSPI-Architektur

SSPI ist eine Softwareschnittstelle. Verteilte Programmierbibliotheken, z. b. RPC, können diese für authentifizierte Kommunikation verwenden. Ein oder mehrere Softwaremodule bieten die eigentlichen Authentifizierungsfunktionen. Jedes Modul, das als Security Support Provider (SSP) bezeichnet wird, wird als Dynamic Link Library (dll) implementiert. Ein SSP stellt mindestens ein Sicherheitspaket bereit.

Es stehen eine Vielzahl von SSPs und Paketen zur Verfügung. Windows umfasst das NTLM-Sicherheitspaket und das Microsoft Kerberos-Protokoll Sicherheitspaket. Außerdem können Sie das Sicherheitspaket Secure Socket Layer (SSL) oder einen beliebigen anderen SSPI-kompatiblen SSP installieren.

Durch die Verwendung von SSPI wird sichergestellt, dass die Anwendung unabhängig davon, welche SSP Sie auswählen, auf einheitliche Weise auf die Authentifizierungs Features zugreift. Diese Funktion bietet Ihrer Anwendung mehr Unabhängigkeit als die Implementierung des Netzwerks, als in der Vergangenheit verfügbar war.

Verteilte Anwendungen kommunizieren über die RPC-Schnittstelle. Die RPC-Software greift wiederum über die SSPI auf die Authentifizierungs Features eines SSP zu.

Weitere Informationen finden Sie unter [SSPI](/windows/desktop/SecAuthN/sspi).

 

 