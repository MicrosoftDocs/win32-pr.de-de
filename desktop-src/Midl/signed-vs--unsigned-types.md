---
title: Signierte und unsignierte Typen (Mittel l)
description: Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- Datentypen-Mittel l, signiert und unsigniert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391358"
---
# <a name="signed-and-unsigned-types-midl"></a>Signierte und unsignierte Typen (Mittel l)

Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen. Sie können diese Probleme vermeiden, indem Sie die Zeichen Typen explizit als signiert oder unsigniert deklarieren. Beachten Sie, dass DCE-IDL-Compiler das Schlüsselwort [**Signed**](signed.md)nicht erkennen. Diese Funktion ist daher nicht verfügbar, wenn Sie den Mittelwert Compiler/**eines Zertifikats** -Schalter verwenden.

In der mittleren l-Datei wird der [**kleine**](small.md) Typ so definiert, dass dasselbe Standard Zeichen wie der [**char**](char-idl.md) -Typ im C-Ziel Compiler übernommen wird. Wenn der Compiler annimmt, dass **char** nicht signiert ist, wird **Small** auch als unsigned definiert. Viele C-Compiler ermöglichen es Ihnen, den Standardwert als Befehlszeilenoption zu ändern. Beispielsweise wird in der Microsoft Visual C++ Entwicklungsumgebung die Befehlszeilenoption **/J** das Standard Zeichen von **char** von signed in unsigned geändert.

Sie können auch das Vorzeichen der Variablen vom Typ " [**char**](char-idl.md) " und " [**Small**](small.md) " mithilfe des Befehls Zeilenschalters " [**/char**](-char.md)" für den Mittelpunkt steuern. Mithilfe dieses Schalters können Sie das von Ihrem Compiler verwendete standardmäßige Vorzeichen angeben. Der mittlerer l-Compiler deklariert explizit das Vorzeichen aller **char** -Typen, die nicht mit dem Standardtyp des C-Compilers in der generierten Header Datei identisch sind.

 

 




