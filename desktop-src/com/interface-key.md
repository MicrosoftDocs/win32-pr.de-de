---
title: Schnittstellenschlüssel
description: Registriert neue Schnittstellen durch Zuordnen eines Schnittstellen namens zu einer Schnittstellen-ID (IID). Es muss ein IID-Unterschlüssel für jede neue Schnittstelle vorhanden sein.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- COM-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037321"
---
# <a name="interface-key"></a>Schnittstellenschlüssel

Registriert neue Schnittstellen durch Zuordnen eines Schnittstellen namens zu einer Schnittstellen-ID (IID). Es muss ein IID-Unterschlüssel für jede neue Schnittstelle vorhanden sein.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ \_ \\ \\ \\ Schnittstelle der Software Klassen der lokalen Maschine** \\ *{* IID *}*



| Registrierungswert                               | BESCHREIBUNG                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Typeinterface wurde**](baseinterface.md)       | Identifiziert die Schnittstelle, von der die aktuelle Schnittstelle abgeleitet wird.                                  |
| [**NumMethods**](nummethods.md)             | Enthält die Anzahl der Methoden in der zugeordneten-Schnittstelle, einschließlich Methoden aus abgeleiteten Schnittstellen. |
| [**Proxystubclsid**](proxystubclsid.md)     | Ordnet eine IID einer CLSID in 16-Bit-Proxy-DLLs zu.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Ordnet eine IID einer CLSID in 32-Bit-Proxy-DLLs zu.                                                           |



 

## <a name="remarks"></a>Bemerkungen

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Berfläche**](interface.md)
</dt> </dl>

 

 




