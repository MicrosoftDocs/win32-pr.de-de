---
title: Implizite und explizite Handles
description: Um ein serialisierungshandle zu deklarieren, verwenden Sie das primitive handle-Typhandle \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858415"
---
# <a name="implicit-vs-explicit-handles"></a>Implizite und explizite Handles

Um ein serialisierungshandle zu deklarieren, verwenden Sie das primitive Handle- [**Typhandle \_ t**](/windows/desktop/Midl/handle-t). Serialisierungshandles können explizit oder implizit sein. Geben Sie mithilfe des **\[ impliziten \_ handle \]** -Attributs implizite Handles in der ACF Ihrer Anwendung an. Der mittlerer l-Compiler generiert eine globale serialisierungshandle-Variable. Serialisierungsprozeduren mit einem impliziten Handle verwenden diese globale Variable, um auf einen gültigen serialisierenden Kontext zuzugreifen.

Bei Verwendung der typcodierung verwenden die generierten Routinen, die die Serialisierung eines bestimmten Typs unterstützen, den globalen impliziten Handle für den Zugriff auf den Serialisierungskontext. Beachten Sie, dass Remote Routinen möglicherweise das implizite Handle als Bindungs Handle verwenden müssen. Stellen Sie sicher, dass das implizite Handle auf ein gültiges serialisierungshandle festgelegt ist, bevor Sie einen serialisierenden-Befehl ausführen.

Ein explizites Handle wird als Parameter des Prototyps der Serialisierungsprozedur in der IDL-Datei angegeben, oder es kann auch mit dem **\[ expliziten \_ handle \]** -Attribut in der ACF angegeben werden. Der explizite handle-Parameter wird verwendet, um den richtigen Serialisierungskontext für die Prozedur festzulegen. Um den korrekten Kontext im Fall der Typserialisierung einzurichten, generiert der Compiler die unterstützenden Routinen, die den expliziten [**handle \_ t**](/windows/desktop/Midl/handle-t) -Parameter als serialisierungshandle verwenden. Sie müssen ein gültiges serialisierungshandle angeben, wenn Sie eine Serialisierungsprozedur oder eine Unterstützungs Routine für den Serialisierungstyp aufrufen.

 

 