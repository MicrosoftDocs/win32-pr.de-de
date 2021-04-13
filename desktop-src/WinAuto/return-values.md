---
title: Rückgabewerte (Windows-Barrierefreiheits Funktionen)
description: In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener angezeigt werden.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474772"
---
# <a name="return-values-windows-accessibility-features"></a>Rückgabewerte (Windows-Barrierefreiheits Funktionen)

In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener angezeigt werden.

## <a name="common-return-values"></a>Allgemeine Rückgabewerte

Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden geben einen der folgenden Werte zurück, die in WinError. h definiert sind, oder einen anderen Standard Component Object Model (com)-Fehlercode:



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | Die Methode wurde erfolgreich ausgeführt.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ false                | Die Methode war teilweise erfolgreich. Dies ist der Fall, wenn die Methode erfolgreich ist, die angeforderten Informationen aber nicht verfügbar sind. Beispielsweise gibt Microsoft Active Accessibility S \_ false zurück, wenn Sie [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) aufrufen, um ein untergeordnetes Objekt an einem bestimmten Punkt abzurufen, und der angegebene Punkt nicht innerhalb des Objekts oder des untergeordneten Objekts liegt. |
| DISP \_ E \_ mitgliednotfound | Das Objekt unterstützt die angeforderte Eigenschaft oder Aktion nicht. Beispielsweise gibt eine Push-Schaltfläche diesen Wert zurück, wenn Sie die [Value-Eigenschaft](value-property.md)anfordern, da Sie nicht über eine Value-Eigenschaft verfügt.                                                                                                                                                                           |
| E \_ notimpl              | Die Methode ist nicht implementiert. Dieser Wert tritt auf, wenn ein Client eine Methode aufruft, die in diesem Betriebssystem noch nicht unterstützt wird.                                                                                                                                                                                                                                                         |
| E \_ invalidArg           | Mindestens ein Argument ist ungültig. Dieser Fehler tritt auf, wenn der Aufrufer versucht, ein untergeordnetes Objekt mithilfe eines Bezeichners zu identifizieren, der vom Server nicht erkannt wird. Dieser Fehler tritt auch dann auf, wenn ein Client versucht, ein untergeordnetes Objekt innerhalb eines Objekts zu identifizieren, das keine untergeordneten Elemente aufweist.                                                                                                      |
| E \_ outo-Memory          | Die Methode konnte keinen Arbeitsspeicher zuweisen, der zum Durchführen eines Vorgangs erforderlich ist, der für den Erfolg entscheidend ist.                                                                                                                                                                                                                                                                                        |
| E \_ fehlschlagen                 | Ein unbekannter oder generischer Fehler ist aufgetreten.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Zusätzliche Rückgabewerte

Im folgenden finden Sie Rückgabewerte, die von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden zurückgegeben werden können. Diese Rückgabewerte sind nicht so häufig wie die vorherigen Werte, Sie sollten sich jedoch bewusst sein.



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ AccessDenied        | Dies wird zurückgegeben, wenn Sie get \_ accValue zum Abrufen des Werts eines Kenn Wort Steuer Elements abrufen. |
| DISP \_ E- \_ Ausnahme     |                                                                                      |
| Co \_ E \_ objnotconnected |                                                                                      |



 

 

 




