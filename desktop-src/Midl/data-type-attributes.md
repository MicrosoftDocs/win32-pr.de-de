---
title: Datentypattribute
description: Sie können diese Attribute auf Datentypen in einer typedef-Anweisung anwenden, um die Verwendung oder Auswirkung des Datentyps weiter zu definieren.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL , Attribute, Datentyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85142c13d9b478c449bf07955b85dd586b6312d891e17699861afb5bc2cc658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067370"
---
# <a name="data-type-attributes"></a>Datentypattribute

Sie können diese Attribute auf Datentypen in einer [**typedef-Anweisung**](typedef.md) anwenden, um die Verwendung oder Auswirkung des Datentyps weiter zu definieren.



| attribute                                 | Verwendung                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kontexthand \_ handle**](context-handle.md) | Identifiziert ein Bindungshand handle, das Zustandsinformationen (Kontextinformationen) auf einem bestimmten Server zwischen Remoteprozeduraufrufen von einem bestimmten Client verwaltet. Ungültig für [**Objektschnittstellenfunktionen.**](object.md)                                                                                                         |
| [**Handlebezeichner**](handle.md)                  | Gibt einen anwendungsspezifischen benutzerdefinierten Handletyp an.                                                                                                                                                                                                                                                                |
| [**ms \_ union**](-ms-union.md)            | Steuert die NDR-Ausrichtung nicht kapselter Unions. Verwenden Sie [**für typedef**](typedef.md)s zur Abwärtskompatibilität mit Schnittstellen, die mit MIDL 1.0 oder 2.0 erstellt wurden.                                                                                                                                                            |
| [**Rohr**](pipe.md)                      | Ermöglicht die Übertragung eines Datenstroms mit offenem Ende von typierten Daten über einen Remoteprozeduraufruf. Ein [**In-Pipe-Parameter**](in.md) ermöglicht es dem Server, den Datenstrom während eines Remoteprozeduraufrufs vom Client zu pullen. Mit [**einem out**](-out.md) pipe-Parameter kann der Server den Datenstrom zurück an den Client übertragen. |
| [**übertragen \_ als**](transmit-as.md)       | Gibt an, wie ein Datentyp über ein Netzwerk übertragen wird, das für benutzerdefiniertes Marshalling verwendet wird.                                                                                                                                                                                                                                  |
| [**\_v1-Aufzählen**](v1-enum.md)               | Gibt an, dass der angegebene enumerierte Typ als 32-Bit-Entität und nicht als 16-Bit-Standard übertragen wird.                                                                                                                                                                                                              |
| [**Wire \_ Marshal**](wire-marshal.md)     | Ähnlich wie [**beim Übertragen \_ als**](transmit-as.md) implementieren Sie die Routinen, um die Daten zu sgrößeren, zu marshallen, zu entmarshalieren und frei zu machen.                                                                                                                                                                                              |



 

 

 




