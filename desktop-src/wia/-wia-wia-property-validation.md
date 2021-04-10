---
description: 'Wenn eine Anwendung einen IPropertyStorage:: Write-Multiple-Vorgang für jede beschreibbare Windows-Abbild Erfassungs Eigenschaft (WIA) ausführt, führt der WIA-Treiber eine Validierung für den neuen Eigenschafts Wert aus.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Überprüfung der WIA-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214640"
---
# <a name="wia-property-validation"></a>Überprüfung der WIA-Eigenschaft

Wenn eine Anwendung einen [IPropertyStorage:: Write-Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) -Vorgang für jede beschreibbare Windows-Abbild Erfassungs Eigenschaft (WIA) ausführt, führt der WIA-Treiber eine Validierung für den neuen Eigenschafts Wert aus. Das Schreiben einer Eigenschaft kann Nebenwirkungen aufweisen, die andere Eigenschaftswerte ändern. Die Anwendung muss alle Eigenschaftswerte nach einem Schreibvorgang lesen, um zu ermitteln, ob alle Eigenschaften auf die von der Anwendung gewünschten Werte festgelegt sind.

Mehrere Eigenschaften können gleichzeitig mit dem [IPropertyStorage:: schreitemultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) -Vorgang geschrieben werden. Möglicherweise gibt es Fälle, in denen einige Eigenschafts Zuweisungen Konflikte verursachen. In solchen Fällen ist die Priorität, die zum Auflösen von Konflikten verwendet wird, wie folgt:

1.  \_ \_ cur- \_ Absicht der WIA-IPS
2.  WIA \_ IPA- \_ DataType
3.  WIA \_ IPA- \_ Tiefe
4.  WIA- \_ IPS- \_ xres
5.  WIA- \_ IPS \_
6.  WIA- \_ IPS- \_ xPos
7.  WIA- \_ IPS ( \_ yPos)
8.  WIA- \_ IPS- \_ XBlock
9.  WIA- \_ IPS \_ yblock

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
