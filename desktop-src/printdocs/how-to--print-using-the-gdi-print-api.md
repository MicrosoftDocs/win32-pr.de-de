---
description: In diesem Thema wird erläutert, wie Sie aus einem nativen Windows-Programm mit dem GDI-&\# 160 Drucken&\# 160; Found.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Vorgehensweise: Drucken mithilfe der GDI-Druck-API'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868535"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Vorgehensweise: Drucken mithilfe der GDI-Druck-API

In diesem Thema wird erläutert, wie Sie mithilfe der [GDI-Druck-API](gdi-printing.md)von einem systemeigenen Windows-Programm drucken.

## <a name="overview"></a>Übersicht

Das Drucken ist in der Regel ein wesentlicher Bestandteil eines systemeigenen Windows-Programms und somit kein Feature, das Sie nach dem Schreiben des Programms problemlos hinzufügen können. Wenn Sie ein Programm für Windows 7 entwerfen, sollten Sie die Verwendung der [XPS-Druck-API](xps-printing.md) in Erwägung gezogen, um die Druck Funktionalität bereitzustellen, da Sie für die Zukunft die meisten Kompatibilitätsfunktionen bietet. Programme, die unter Windows Vista und früheren Versionen von Windows ausgeführt werden müssen, verwenden wahrscheinlich die [GDI-Druck-API](gdi-printing.md) , um Druck Funktionalität bereitzustellen. Die GDI-Druck-API wird auch in Windows 7 unterstützt, ist aber eingeschränkter als die XPS-Druck-API.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Drucken](using-printing.md)
</dt> <dt>

[Drucken aus einer Windows-Anwendung](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



