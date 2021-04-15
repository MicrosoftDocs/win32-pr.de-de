---
title: Was wird von einem Client angezeigt?
description: Dieses Thema listet Möglichkeiten auf, wie ein Client ADSI-Daten anzeigt.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, was wird von einem Client angezeigt?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517108"
---
# <a name="what-does-a-client-see"></a>Was wird von einem Client angezeigt?

-   Ein Client sieht ADSI und alle seine Erweiterungs Objekte als ein Objekt.
-   Ein ADSI-Client sieht eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle, die alle Dual-und Dispatch-Schnittstellen im-Objekt verarbeitet, unabhängig davon, ob die Dual-oder Dispatch-Schnittstelle vom Aggregator im Anbieter oder durch eine Erweiterung implementiert wird. Weitere Informationen finden Sie unter [Auflösung von Konflikten bei Funktions-/Eigenschaftennamen in Automation](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   ADSI macht keine Typinformationen über die [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) -Methode oder die [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) -Methode verfügbar. ADSI stellt Typinformationen über die Typbibliothek bereit.

 

 