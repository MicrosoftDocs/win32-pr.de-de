---
description: Wenn eine Anwendung einen IPropertyStorage::WriteMultiple-Vorgang für jede schreibbare Windows WIA-Eigenschaft (Image Acquisition) ausführt, führt der WIA-Treiber eine Überprüfung des neuen Eigenschaftswerts durch.
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: WIA-Eigenschaftenüberprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1aca5879dbcb789b7e94a780c8fc99e53b703f6aea74498ae455e8e2ec6b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813050"
---
# <a name="wia-property-validation"></a>WIA-Eigenschaftenüberprüfung

Wenn eine Anwendung einen [IPropertyStorage::WriteMultiple-Vorgang](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) für jede schreibbare Windows WIA-Eigenschaft (Image Acquisition) ausführt, führt der WIA-Treiber eine Überprüfung des neuen Eigenschaftswerts aus. Das Schreiben einer Eigenschaft hat möglicherweise Seitenauswirkung, die andere Eigenschaftswerte ändern. Es liegt an der Anwendung, alle Eigenschaftswerte nach einem Schreibvorgang zu lesen, um zu bestimmen, dass alle Eigenschaften auf Werte festgelegt sind, die die Anwendung wünscht.

Mehrere Eigenschaften können gleichzeitig mithilfe des [IPropertyStorage::WriteMultiple-Vorgangs](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) geschrieben werden. Es kann Fälle geben, in denen einige Eigenschaftenzuweisungen in Konflikt stehen. In solchen Fällen lautet die Priorität, die zum Lösen von Konflikten verwendet wird, wie folgt:

1.  WIA \_ IPS \_ CUR \_ INTENT
2.  WIA \_ \_ IPA-DATENTYP
3.  WIA \_ \_ IPA-TIEFE
4.  WIA \_ IPS \_ XRES
5.  WIA \_ IPS \_ YRES
6.  WIA \_ IPS \_ XPOS
7.  WIA \_ IPS \_ YPOS
8.  WIA \_ IPS \_ XEXTENT
9.  WIA \_ IPS \_ YEXTENT

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
