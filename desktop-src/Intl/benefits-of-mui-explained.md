---
description: Vorteile von EXPLAINed
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Vorteile von EXPLAINed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971f66ef7fc094912e87d7e9ab77284fecb0931d9222e6910931b281b6308286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829699"
---
# <a name="benefits-of-mui-explained"></a>Vorteile von EXPLAINed

-   [BENEFITS-Vorteile für Entwickler](#mui-benefits-for-developers)
-   [BENEFITS-Vorteile für Unternehmen](#mui-benefits-for-enterprises)
-   [BENEFITS-Vorteile für OEMs](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>BENEFITS-Vorteile für Entwickler

Es gibt viele möglichkeiten, eine SOLUTIONS-Lösung in Anwendungen zu implementieren, aber jede Möglichkeit ist eine Variation von einer von drei grundlegenden Methoden:

1.  Kompilieren einer Binärdatei (mit integrierten Ressourcen) für jede Sprache. Dies ist der *De-facto-Standard* für Legacyanwendungen, da dies das primäre Modell ist, das von Standardentwicklungstools wie Microsoft Visual Studio unterstützt wird. Dieses Modell erfordert mehrere Binärdateien für mehrere Sprachen und weist Einschränkungen in Bezug auf die Bereitstellung einzelner Images und mehrsprachige Szenarien auf. Beachten Sie, dass anwendungen, die mit diesem Modell entwickelt wurden, weiterhin an Windows Vista funktionieren und dass Tools bereitgestellt werden, mit denen Entwickler von diesem Modell zum moderneren Modell wechseln können, das in der dritten Methode beschrieben wird.
2.  Sie verfügen über eine sprachneutrale Kernbinärdatei mit einer dll (Dynamic Link Library) für mehrsprachige Ressourcen. Dieses Modell ist definitiv SEHR benutzerfreundlicher, macht es jedoch schwierig, die Ressourcenbinärdateien für neue Sprachen zu aktualisieren. Angenommen, Sie möchten neben Englisch, Französisch und Japanisch auch Deutsch unterstützen. Eine ganz neue Ressourcenbinärdatei muss für Ihre Benutzer bereitgestellt und bereitgestellt werden, die möglicherweise nicht unbedingt Deutsch benötigen.
3.  Eine sprachneutrale Kernbinärdatei mit einem Satz von Ressourcen-DLLs pro Sprache. Auf diese Weise wird das Betriebssystem selbst in Windows Vista implementiert, und Entwicklern wird empfohlen, dieses Modell für Anwendungen zu verwenden, da es mehr als die beiden vorherigen Modelle bietet.

Vor der Windows Vista-Version war die Einführung aufgrund der fehlenden integrierten Unterstützung für dieses letztere Modell schwierig. Dies hat sich jedoch geändert, und die Vorteile dieses Modells sind zahlreich und machen es zu einem hervorragenden Modell für Ihre Anwendungen:

-   Anwendungen können mehrsprachig sein und sich auf die gleiche Weise wie Windows Vista verhalten, wodurch eine konsistente Anzeigesprache für Benutzer bereitgestellt wird.
-   Die Flexibilität beim Freigeben zusätzlicher Sprachen für eine Anwendung wird erhöht. Zusätzliche Sprachen können unabhängig vom Kerncode freigegeben werden. Dies bedeutet, dass die Unterstützung für neue Sprachen im Laufe der Zeit nach Bedarf hinzugefügt werden kann.
-   Die Kosten für die Erstellung und Wartung weiterer Sprachversionen werden reduziert.
-   OEMs und Unternehmen können Anwendungen problemlos in ihr globalisiertes PC-Image integrieren– bereit für den Versand in verschiedene Länder.
-   Tools und Richtlinien, die Sie bei der Migration Ihrer Anwendung zum Windows Vista VISTA-MODELL unterstützen, sind verfügbar. Insbesondere stellt MSDN einen [umfangreichen Satz an Dokumentationen](multilingual-user-interface.md) zu MSDN bereit.

## <a name="mui-benefits-for-enterprises"></a>BENEFITS-Vorteile für Unternehmen

DIESE bietet zwei hauptvorteile für Unternehmen:

-   Installation einzelner Images: MIT DER MÖGLICHKEIT können Unternehmen dasselbe image weltweit (oder in einem beliebigen Teil davon) mit einer einzigen Installation rollouten, unterstützen und warten. Windows Vista erweitert den Rollout des Betriebssystems mit einem einzelnen Image, sodass Geschäftsanwendungen auch als Teil desselben Images bereitgestellt werden können.
-   Unterstützung mehrsprachiger Desktops: Mehrere lokalisierte UI-Sprachpakete können auf einem Desktop installiert werden, wodurch mehrere Benutzer einen einzelnen Desktop freigeben können, während sie weiterhin ihre eigenen bevorzugten Benutzeroberflächensprachen verwenden. Dies gilt auch für öffentliche Computer, die für alle offiziell gesprochenen Sprachen gleich behandelt werden müssen (z. B. in Kanada und in der Europäischen Union) sowie für freigegebene Computer für Roamingbenutzer.

## <a name="mui-benefits-for-oems"></a>BENEFITS-Vorteile für OEMs

Der Hauptvorteil für OEMs ist die installation einzelner Images, die VON AKTIVIERT wird, da sie es ermöglicht, Images zu erstellen, die alle erforderlichen Sprachen enthalten, um eine geografische Zone effektiv als Ziel festzulegen, und die Sprachauswahl auf die Erstinstallation des Computers durch den Benutzer zu verzögern. Dies ermöglicht insbesondere eine effektivere Verwaltung des Bestands für OEMs.

Durch die Bereitstellung von SUPPORTS für Anwendungen ermöglicht Windows Vista oeMs auch, Mehrwertanwendungen für ihre Images bereitzustellen und gleichzeitig von der Installation eines einzelnen Images zu profitieren, solange diese Anwendungen AKTIVIERT sind.

 

 



