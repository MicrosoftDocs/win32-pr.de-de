---
title: Behandeln von Dienstobjektfehlern
description: Wenn ein Fehler in einem Dienstobjekt auftritt, sollte der Rückgabewert für den Aufruf von IDispatch Invoke DISP \_ E \_ EXCEPTION sein, und der pExceptInfo-Parameterzeiger auf eine EXCEPTINFO-Struktur in der sollte ausgefüllt werden.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c98db4ffdb3c4625ec4c0dfbe3d497ab1cbe4b5152b172c34422c1630ce581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999520"
---
# <a name="service-object-error-handling"></a>Behandeln von Dienstobjektfehlern

Wenn in einem Dienstobjekt ein Fehler auftritt, sollte der Rückgabewert für den Aufruf [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) DISP \_ E EXCEPTION \_ sein, und der *pExceptInfo-Parameterzeiger* auf eine [**EXCEPTINFO-Struktur**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) in der sollte ausgefüllt werden.

Insbesondere werden die Member **bstrSource** und **bstrDescription** der [**EXCEPTINFO-Struktur**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) vom Gerätehost mit UPnP-Technologie verwendet, um eine UPnP-Fehlerantwort zu erstellen. **bstrSource** ist der Fehlercode, und **bstrDescription** ist die Fehlerbeschreibung.

 

 