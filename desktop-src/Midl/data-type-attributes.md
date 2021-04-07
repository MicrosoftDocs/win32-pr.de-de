---
title: Datentyp Attribute
description: Sie können diese Attribute auf Datentypen in einer typedef-Anweisung anwenden, um die Verwendung oder den Effekt des Datentyps weiter zu definieren.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL-Mittell, Attribute, Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714369"
---
# <a name="data-type-attributes"></a>Datentyp Attribute

Sie können diese Attribute auf Datentypen in einer [**typedef**](typedef.md) -Anweisung anwenden, um die Verwendung oder den Effekt des Datentyps weiter zu definieren.



| Attribut                                 | Verbrauch                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kontext \_ handle**](context-handle.md) | Identifiziert ein Bindungs handle, das Statusinformationen (Kontextinformationen) auf einem bestimmten Server zwischen Remote Prozedur Aufrufen von einem bestimmten Client verwaltet. Nicht gültig für [**Objekt**](object.md) Schnittstellen Funktionen.                                                                                                         |
| [**bewältigen**](handle.md)                  | Gibt einen spezifischen Handlertyp an, der für die Anwendung spezifisch ist.                                                                                                                                                                                                                                                                |
| [**MS- \_ Union**](-ms-union.md)            | Steuert die NDR-Ausrichtung von nicht gekapselten Unions. Verwenden Sie für die Verwendung von [**typedef**](typedef.md)s, um die Abwärtskompatibilität mit Schnittstellen zu verwenden, die mit der Mittell 2,0 1,0                                                                                                                                                            |
| [**Kanal**](pipe.md)                      | Ermöglicht die Übertragung eines geöffneten Datenstroms für typisierte Daten über einen Remote Prozedur Aufruf. Ein [**in**](in.md) Pipe-Parameter ermöglicht dem Server das Abrufen des Datenstroms vom Client während eines Remote Prozedur Aufrufes. Ein Out-Pipe-Parameter ermöglicht es dem Server, den Datenstrom an den Client zurück [**zusenden**](-out.md) . |
| [**übertragen \_ als**](transmit-as.md)       | Gibt an, wie ein Datentyp über ein Netzwerk übertragen wird, das für das benutzerdefinierte Marshalling verwendet wird.                                                                                                                                                                                                                                  |
| [**v1-Aufzählung \_**](v1-enum.md)               | Weist an, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standardwert übertragen wird.                                                                                                                                                                                                              |
| [**Wire \_ Marshal**](wire-marshal.md)     | Ähnlich wie bei der über [**Tragung \_ als**](transmit-as.md) , aber implementieren Sie die Routinen, um die Daten zu verkleinern, zu Mars Hallen, zu entsperren und freizugeben.                                                                                                                                                                                              |



 

 

 




