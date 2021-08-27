---
description: Anwendungen sehen Windows WIA-Geräte (Image Acquisition) als hierarchische Struktur von IWiaItem- oder IWiaItem2-Objekten mit dem Stammelement, das das Gerät selbst darstellt.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: WIA Minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e8d3c520106c345bd02df5b686bb1abf34f9ff1aa0b338e645b178cabbb874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056920"
---
# <a name="wia-minidriver"></a>WIA Minidriver

Anwendungen sehen Windows WIA-Geräte (Image Acquisition) als hierarchische Struktur von [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) mit dem Stammelement, das das Gerät selbst darstellt. WIA-Geräte können von mehreren Anwendungen gleichzeitig verwendet werden. Daher muss die Ansicht einer Anwendung eines **IWiaItem-** oder **IWiaItem2-Objekts** unabhängig von den Ansichten einer anderen Anwendung sein. Dies wird erreicht, indem zwei verschiedene Elementobjekte verwendet werden. Der Treiber erstellt die Treiberelementstruktur von [IWiaDrvItem-Schnittstellenobjekten,](https://msdn.microsoft.com/library/ms793976.aspx) die auch als Treiberelemente bezeichnet werden, mithilfe der WIA-Treiberdienstmethoden. Dies sind globale Objekte, die der Treiber verwendet, um die internen Elemente jedes Treibers darzustellen. Wenn eine Anwendung ein **IWiaItem-** oder **IWiaItem2-Objekt** (auch als Anwendungselement bezeichnet) erstellt, wird dieses Objekt mit der entsprechenden [IWiaDrvItem-Schnittstelle](https://msdn.microsoft.com/library/ms793976.aspx) des Treibers in der Treiberelementstruktur verknüpft. Ein Verweiszähler wird für das [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) gemäß den folgenden Regeln beibehalten:

-   Wenn ein Treiber der Treiberelementstruktur ein [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) hinzufügt, wird die Verweisanzahl des [IWiaDrvItem-Schnittstellenobjekts](https://msdn.microsoft.com/library/ms793976.aspx) erhöht. Dies erfolgt in der Regel während [IWiaMiniDrv::d rvInitializeWia](https://msdn.microsoft.com/library/ms794097.aspx) oder beim Verarbeiten eines WIA \_ CMD \_ SYNCHRONIZE-Befehls.
-   Wenn ein Treiber ein [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) aus der Treiberelementstruktur entfernt, wird der Verweiszähler des [IWiaDrvItem-Schnittstellenobjekts](https://msdn.microsoft.com/library/ms793976.aspx) dekrementiert, und das [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) wird markiert, sodass es nicht erneut auf das Gerät zugreifen kann. Dies geschieht in der Regel, wenn ein Gerät getrennt oder ein Element gelöscht wird. Anwendungen können weiterhin Eigenschaften aus einem [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) lesen, auch wenn das entsprechende [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) aus der Treiberelementstruktur entfernt wurde.
-   Wenn ein [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) erstellt wird, wird es mit einem entsprechenden [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) verknüpft. Der Verweiszähler des [IWiaDrvItem-Schnittstellenobjekts](https://msdn.microsoft.com/library/ms793976.aspx) wird erhöht.
-   Wenn ein [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) freigegeben wird, wird der Link zum entsprechenden [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) getrennt, und der Verweiszähler des [IWiaDrvItem-Schnittstellenobjekts](https://msdn.microsoft.com/library/ms793976.aspx) wird dekrementiert.
-   Wenn der Verweiszähler eines [IWiaDrvItem-Schnittstellenobjekts](https://msdn.microsoft.com/library/ms793976.aspx) auf 0 (null) fällt, wird das [IWiaDrvItem-Schnittstellenobjekt](https://msdn.microsoft.com/library/ms793976.aspx) gelöscht. Dies gilt für alle [IWiaDrvItem-Schnittstellenobjekte](https://msdn.microsoft.com/library/ms793976.aspx) einschließlich des Stammelements. Der Verweiszähler eines [IWiaDrvItem-Schnittstellenobjekts](https://msdn.microsoft.com/library/ms793976.aspx) wird nur auf 0 (null) festgelegt, wenn keine Anwendungselemente darauf verweisen und nicht mehr mit der Treiberelementstruktur verknüpft sind.

Mit diesem Verweiszählungsschema können viele [**IWiaItem-**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) oder [**IWiaItem2-Objekte**](-wia-iwiaitem2.md) ohne Beeinträchtigung mit einer [IWiaDrvItem-Schnittstelle](https://msdn.microsoft.com/library/ms793976.aspx) verknüpft werden. Da jedes **IWiaItem-** oder **IWiaItem2-Element** seinen eigenen Eigenschaftenspeicher enthält, kann eine Anwendung auch nach dem Löschen eines Elements weiterhin Elementeigenschaften lesen, aber kein Vorgang, der Zugriff auf das Gerät erfordert, ist erfolgreich. Da Elementeigenschaften im **IWiaItem-** oder **IWiaItem2-Objekt** gespeichert werden, muss der Treiber die Eigenschaften des **IWiaItem-** oder **IWiaItem2-Objekts** vor einer Datenübertragung auf das Gerät festlegen.

 

 



