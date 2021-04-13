---
description: Anwendungen sehen Windows-Abbild Erfassungsgeräte (WIA) als hierarchische Struktur von iwiaitem-oder IWiaItem2-Objekten mit dem Stamm Element, das das eigentliche Gerät darstellt.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: WIA-Mini Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aadaf55cfe2e8102d4e0e02cf9787b9696e327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526411"
---
# <a name="wia-minidriver"></a>WIA-Mini Treiber

Anwendungen sehen Windows-Abbild Erfassungsgeräte (WIA) als hierarchische Struktur von [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten mit dem Stamm Element, das das eigentliche Gerät darstellt. WIA-Geräte können gleichzeitig von mehr als einer Anwendung verwendet werden. Daher ist es erforderlich, dass die Ansichten der einzelnen Anwendungen von **iwiaitem** -oder **IWiaItem2** -Objekten unabhängig von den Sichten einer anderen Anwendung sind. Dies wird erreicht, indem zwei unterschiedliche Element Objekte vorhanden sind. Der Treiber erstellt mithilfe der WIA driver Services-Methoden die Treiber Elementstruktur von [iwiadrvitem Interface](https://msdn.microsoft.com/library/ms793976.aspx) Objects, auch als Treiber Elemente bezeichnet. Dabei handelt es sich um globale Objekte, die der Treiber zum Darstellen der internen Elemente jedes Treibers verwendet. Wenn eine Anwendung ein **iwiaitem** -oder **IWiaItem2** -Objekt (auch als Anwendungs Element bezeichnet) erstellt, wird dieses Objekt mit der entsprechenden [iwiadrvitem-Schnittstelle](https://msdn.microsoft.com/library/ms793976.aspx) des Treibers in der Treiber Elementstruktur verknüpft. Für das [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt, das den folgenden Regeln unterliegt, wird ein Verweis Zähler beibehalten:

-   Wenn ein Treiber der Treiber Elementstruktur ein [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt hinzufügt, wird der Verweis Zähler des [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekts inkrementiert. Dies erfolgt in der Regel bei [iwiaminidrv::d rvinitializewia](https://msdn.microsoft.com/library/ms794097.aspx) oder bei der Verarbeitung eines WIA \_ cmd- \_ Befehls zum Synchronisieren.
-   Wenn ein Treiber ein [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt aus der Treiber Elementstruktur entfernt, wird der Verweis Zähler des [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekts dekrementiert, und das [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt ist so gekennzeichnet, dass es nicht mehr auf das Gerät zugreifen kann. Dies geschieht in der Regel, wenn ein Gerät getrennt oder ein Element gelöscht wird. Anwendungen können weiterhin Eigenschaften aus einem [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt lesen, auch wenn das zugehörige [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt aus der Treiber Elementstruktur entfernt wurde.
-   Wenn ein [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt erstellt wird, wird es mit einem entsprechenden [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt verknüpft. Der Verweis Zähler des [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekts wird inkrementiert.
-   Wenn ein [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt freigegeben wird, wird der Link zum entsprechenden [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt getrennt, und der Verweis Zähler des [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekts wird dekrementiert.
-   Wenn der Verweis Zähler eines [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekts auf NULL wechselt, wird das [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekt gelöscht. Dies gilt für alle [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekte einschließlich des Stamm Elements. Der Verweis Zähler eines [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Objekts wird nur auf 0 (null) gesetzt, wenn keine Anwendungs Elemente darauf verweisen und es nicht mehr mit der Treiber Elementstruktur verknüpft ist.

Mit diesem Verweis Zählschema können viele [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte ohne Störungen mit einer [iwiadrvitem-Schnittstelle](https://msdn.microsoft.com/library/ms793976.aspx) verknüpft werden. Da jedes **iwiaitem** oder **IWiaItem2** seinen eigenen Eigenschafts Speicher enthält, kann eine Anwendung weiterhin Element Eigenschaften lesen, auch nachdem ein Element gelöscht wurde, aber es ist kein Vorgang erforderlich, der Zugriff auf das Gerät erfordert. Da Element Eigenschaften im **iwiaitem** -oder **IWiaItem2** -Objekt gespeichert werden, muss der Treiber die Eigenschaften des **iwiaitem** -oder **IWiaItem2** -Objekts vor einer Datenübertragung auf das Gerät festlegen.

 

 



