---
title: Was sieht ein Client?
description: In diesem Thema werden Möglichkeiten aufgeführt, wie ein Client ADSI-Daten anzeigen kann.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- Extensions ADSI , was wird einem Client angezeigt?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d38563de47cfc80bdcf265249bf3e4cf10bc46471e18672221fed8c3047efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082174"
---
# <a name="what-does-a-client-see"></a>Was sieht ein Client?

-   Ein Client sieht ADSI und alle seine Erweiterungsobjekte als ein Objekt.
-   Ein ADSI-Client sieht eine [**IDispatch-Schnittstelle,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die alle Dual- und Dispatch-Schnittstellen im Objekt verarbeitet, unabhängig davon, ob die Dual- oder Dispatch-Schnittstelle vom Aggregator im Anbieter oder durch eine Erweiterung implementiert wird. Weitere Informationen finden [Sie unter Lösen von Funktions-/Eigenschaftsnamenkonflikten in Automation in Erweiterungen.](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)
-   ADSI macht keine Typinformationen über die [**Methoden IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) oder [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) verfügbar. ADSI stellt Typinformationen über die Typbibliothek zur Verfügung.

 

 