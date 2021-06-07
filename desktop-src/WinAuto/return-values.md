---
title: Rückgabewerte (Windows-Barrierefreiheitsfeatures)
description: In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener zu sehen sind.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443991"
---
# <a name="return-values-windows-accessibility-features"></a>Rückgabewerte (Windows-Barrierefreiheitsfeatures)

In diesem Thema werden die gängigsten Rückgabewerte und andere Rückgabewerte beschrieben, die möglicherweise seltener zu sehen sind.

## <a name="common-return-values"></a>Allgemeine Rückgabewerte

Die [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) geben einen der folgenden Werte zurück, der in winerror.h definiert ist, oder einen anderen standard Component Object Model (COM)-Fehlercode:



|   Wert                      |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | Die Methode wurde erfolgreich ausgeführt.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ FALSE                | Die -Methode war teilweise erfolgreich. Dies geschieht, wenn die Methode erfolgreich ist, die angeforderten Informationen jedoch nicht verfügbar sind. Beispielsweise gibt Microsoft Active Accessibility S FALSE zurück, wenn Sie \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) aufrufen, um ein untergeordnetes Objekt an einem bestimmten Punkt abzurufen, und der angegebene Punkt nicht innerhalb des Objekts oder des untergeordneten Objekts liegt. |
| DISP \_ E \_ MEMBERNOTFOUND | Das -Objekt unterstützt die angeforderte Eigenschaft oder Aktion nicht. Beispielsweise gibt eine Pushschaltfläche diesen Wert zurück, wenn Sie die [Value-Eigenschaft](value-property.md)anfordern, da sie keine Value-Eigenschaft hat.                                                                                                                                                                           |
| E \_ NOTIMPL              | Die Methode ist nicht implementiert. Dieser Wert tritt auf, wenn ein Client eine Methode aufruft, die in diesem Betriebssystem noch nicht unterstützt wird.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Mindestens ein Argument war ungültig. Dieser Fehler tritt auf, wenn der Aufrufer versucht, ein untergeordnetes Objekt mithilfe eines Bezeichners zu identifizieren, der vom Server nicht erkannt wird. Dieser Fehler tritt auch auf, wenn ein Client versucht, ein untergeordnetes Objekt in einem Objekt zu identifizieren, das keine untergeordneten Objekte enthält.                                                                                                      |
| E \_ OUTOFMEMORY          | Die -Methode konnte keinen Arbeitsspeicher zuordnen, der zum Abschließen eines vorgangs erforderlich ist, der für den Erfolg entscheidend ist.                                                                                                                                                                                                                                                                                        |
| E \_ FAIL                 | Unbekannter oder generischer Fehler.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Zusätzliche Rückgabewerte

Im Folgenden finden Sie Rückgabewerte, die [**IAccessible-Methoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) zurückgeben können. Diese Rückgabewerte sind nicht so häufig wie die vorherigen, aber Sie sollten sie kennen.



|    Wert                    |    BESCHREIBUNG                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSDENIED        | Dies wird zurückgegeben, wenn Sie get \_ accValue aufrufen, um den Wert eines Kennwortsteuerworts zu erhalten. |
| DISP \_ E \_ EXCEPTION     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




