---
description: Ein einzelnes Matrixobjekt kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Bedeutung der Transformationsreihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8a7c0c840fa5c2debaccef4450c525bab8cf7f6e4373653eadaf53a6538891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359580"
---
# <a name="why-transformation-order-is-significant"></a>Bedeutung der Transformationsreihenfolge

Ein [**einzelnes Matrixobjekt**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) kann eine einzelne Transformation oder eine Sequenz von Transformationen speichern. Letzteres wird als *zusammengesetzte Transformation**bezeichnet.*   Die Matrix einer zusammengesetzten Transformation wird durch Multiplizieren der Matrizen der einzelnen Transformationen ermittelt.

In einer zusammengesetzten Transformation ist die Reihenfolge der einzelnen Transformationen wichtig. Wenn Sie z. B. zuerst drehen, dann skalieren und dann übersetzen, erhalten Sie ein anderes Ergebnis als wenn Sie zuerst übersetzen, dann drehen und dann skalieren. In Windows GDI+ werden zusammengesetzte Transformationen von links nach rechts erstellt. Wenn S, R und T Skalierungs-, Dreh- und Übersetzungsmatrizen sind, ist das Produkt SRT (in dieser Reihenfolge) die Matrix der zusammengesetzten Transformation, die zuerst skaliert, dann gedreht und dann übersetzt wird. Die vom Produkt SRT erzeugte Matrix ist anders als die vom Produkt TRS erzeugte Matrix.

Ein Wichtiger Grund ist, dass Transformationen wie Drehung und Skalierung in Bezug auf den Ursprung des Koordinatensystems durchgeführt werden. Das Skalieren eines Objekts, das am Ursprung zentriert ist, führt zu einem anderen Ergebnis als das Skalieren eines Objekts, das vom Ursprung entfernt wurde. Ebenso ergibt das Drehen eines Objekts, das am Ursprung zentriert ist, ein anderes Ergebnis als das Drehen eines Objekts, das vom Ursprung entfernt wurde.

Im folgenden Beispiel werden Skalierung, Drehung und Übersetzung (in dieser Reihenfolge) kombiniert, um eine zusammengesetzte Transformation zu bilden. Das Argument ["MatrixOrderAppend",](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) das an die [**Graphics::RotateTransform-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) übergeben wird, gibt an, dass die Drehung der Skalierung folgt. Ebenso gibt das Argument ["MatrixOrderAppend",](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) das an die [**Graphics::TranslateTransform-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) übergeben wird, an, dass die Übersetzung der Drehung folgt.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Im folgenden Beispiel werden die gleichen Methodenaufrufe wie im vorherigen Beispiel verwendet, aber die Reihenfolge der Aufrufe wird umgekehrt. Die resultierende Reihenfolge der Vorgänge wird zuerst übersetzt, dann gedreht und dann skaliert, was ein sehr anderes Ergebnis als die erste Skalierung erzeugt, dann rotiert und dann übersetzt wird:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Eine Möglichkeit, die Reihenfolge der einzelnen Transformationen in einer zusammengesetzten Transformation umzukehren, besteht in der Umkehrung der Reihenfolge einer Sequenz von Methodenaufrufen. Eine zweite Möglichkeit, die Reihenfolge der Vorgänge zu steuern, besteht in der Änderung des Matrix reihenfolgenarguments. Das folgende Beispiel ist identisch mit dem vorherigen Beispiel, mit der Ausnahme, dass ["MatrixOrderAppend""](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) in ["MatrixOrderPrepend" geändert wurde.](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) Die Matrixmultiplikation erfolgt in der Reihenfolge SRT, wobei S, R und T die Matrizen für Skalierung, Drehung und Übersetzung sind. Die Reihenfolge der zusammengesetzten Transformation wird zuerst skaliert, dann gedreht und dann übersetzt.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



Das Ergebnis des vorherigen Beispiels ist das gleiche Ergebnis, das wir im ersten Beispiel dieses Abschnitts erzielt haben. Dies liegt daran, dass wir sowohl die Reihenfolge der Methodenaufrufe als auch die Reihenfolge der Matrixmultiplikation umgekehrt haben.

 

 



