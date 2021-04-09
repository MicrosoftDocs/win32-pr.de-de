---
title: Typen mit und ohne Vorzeichen (RPC)
description: Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858606"
---
# <a name="signed-and-unsigned-types-rpc"></a>Typen mit und ohne Vorzeichen (RPC)

Compiler, die unterschiedliche Standardwerte für Typen mit und ohne Vorzeichen verwenden, können zu Softwarefehlern in der verteilten Anwendung führen. Sie können diese Probleme vermeiden, indem Sie die Zeichen Typen explizit als **signiert** oder **unsigniert** deklarieren.

In der mittleren l-Datei wird der [**kleine**](/windows/desktop/Midl/small) Typ so definiert, dass dasselbe Standard Zeichen wie der **char** -Typ im C-Ziel Compiler übernommen wird. Wenn der Compiler annimmt, dass **char** nicht signiert ist, wird **Small** auch als unsigned definiert. Viele C-Compiler ermöglichen es Ihnen, den Standardwert als Befehlszeilenoption zu ändern. Beispielsweise ändert die Befehlszeilenoption Microsoft C Compiler **/J** das Standard Zeichen von **char** von signed in unsigned.

Sie können auch das Vorzeichen der Variablen vom Typ " **char** " und " **Small** " mithilfe des Befehls Zeilenschalters " [**/char**](/windows/desktop/Midl/-char)" für den Mittelpunkt steuern. Mithilfe dieses Schalters können Sie das von Ihrem Compiler verwendete standardmäßige Vorzeichen angeben. Der mittlerer l-Compiler deklariert explizit das Vorzeichen aller **char** -Typen, die nicht mit dem Standardtyp des C-Compilers in der generierten Header Datei identisch sind.

 

 
