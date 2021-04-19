---
description: Bei der Media Service Provider Interface (MSPi) handelt es sich um einen Satz von Schnittstellen und Methoden, die von einem MSP implementiert werden, um eine TAPI 3-Anwendungssteuerung über Medien Transport während einer Kommunikationssitzung zuzulassen.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: Media Service Provider Interface (MSPi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1ce09e626ede14515c0abbbd5c3a35921026d6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355722"
---
# <a name="media-service-provider-interface-mspi"></a>Media Service Provider Interface (MSPi)

Bei der Media Service Provider Interface (MSPi) handelt es sich um einen Satz von Schnittstellen und Methoden, die von einem MSP implementiert werden, um eine TAPI 3-Anwendungssteuerung über Medien Transport während einer Kommunikationssitzung zuzulassen. Ein MSP verarbeitet die gerätespezifischen und Protokoll spezifischen Mechanismen, die zum Ausführen dieser Steuerelemente erforderlich sind, und kommuniziert mithilfe der in der MSPi bereitgestellten Methoden mit dem gekoppelten TSP oder einer Anwendung.

Der folgende Abschnitt ( [Referenz zur Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-reference.md)) enthält Details zu den Schnittstellen, die ein MSP verfügbar macht, um mit der Microsoft-Telefonieumgebung zu interagieren.

Außerdem kann ein MSP anbieterspezifische private Schnittstellen und Methoden zur weiteren Unterstützung der Mediensteuerung verfügbar machen. Beispielsweise macht die [MSP der IP-Konferenz](ipconf-msp.md) Schnittstellen verfügbar, die Teilnehmer Steuerung bereitstellen. Weitere Informationen zur Funktionsweise privater Objekte und [ipconf MSP-Schnittstellen](ipconf-msp-interfaces.md) für eine Verweis Auflistung von ipconf finden Sie unter [anbieterspezifische Schnittstellen](provider-specific-interfaces.md) .

Der Großteil der Programmier Bemühungen bei der Erstellung eines MSP ist sehr spezifisch für eine bestimmte Plattform, ein Gerät und ein Transportprotokoll und liegt außerhalb des Umfangs dieses Dokuments. Microsoft stellt jedoch eine Reihe von MSP-Basisklassen bereit, die für die meisten MSP-Autoren nützlich sein werden. Weitere Informationen zur Verwendung dieser Klassen finden Sie unter [TAPI 3 MSP-Basisklassen](tapi-3-msp-base-classes.md) .

Die [**itmspaddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) -Schnittstelle stellt einen Medien Dienstanbieter für die TAPI-dll dar. Diese Schnittstelle wird nicht von oder für eine Endbenutzer Anwendung verwendet. Die TAPI 3-dll ruft **cokreateinstance** für diese Schnittstelle auf, um das Haupt-MSP-Objekt zu erstellen. Mithilfe von Methoden für dieses Objekt kann eine Anwendung das MSP laden und entladen, Informationen von einem TSP empfangen und die [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) -Schnittstelle erstellen, die für das calltobjekt verfügbar gemacht wird.

Die Schnittstellen [**itsubstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) und [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) stellen parallele Methoden in Bezug auf die unter Ströme bereit. Die Unterstützung von Substreams ist optional. Alle anderen Schnittstellen müssen von einem MSP implementiert werden.

> [!Note]  
> Von einem TSP-/MSP-paar implementierte Vorgänge müssen sich in einer DLL befinden, damit Benutzer den Dienstanbieter aktualisieren können, ohne das System neu starten zu müssen.

 

 

 
