---
title: Implizite und explizite Handles
description: Verwenden Sie zum Deklarieren eines Serialisierungshandpunkts das handle t des primitiven \_ Handletyps.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9f6dabc8a6e4d0e5ccac7ac8b94e1812d81a674b471015c868b32209fd9746
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020460"
---
# <a name="implicit-vs-explicit-handles"></a>Implizite und explizite Handles

Um ein Serialisierungshand handle zu deklarieren, verwenden Sie das primitive [**Handletyphand \_ handle t**](/windows/desktop/Midl/handle-t). Serialisierungshandles können explizit oder implizit sein. Geben Sie implizite Handles im ACF Ihrer Anwendung an, indem Sie das **\[ implizite \_ Handleattribut \]** verwenden. Der MIDL-Compiler generiert eine globale Serialisierungshandlevariable. Serialisierungsvorgänge mit einem impliziten Handle verwenden diese globale Variable, um auf einen gültigen Serialisierungskontext zu zugreifen.

Bei Verwendung der Typcodierung verwenden die generierten Routinen, die die Serialisierung eines bestimmten Typs unterstützen, das globale implizite Handle für den Zugriff auf den Serialisierungskontext. Beachten Sie, dass Remoteroutinen möglicherweise das implizite Handle als Bindungshand handle verwenden müssen. Stellen Sie sicher, dass das implizite Handle auf ein gültiges Serialisierungshand handle festgelegt ist, bevor Sie einen Serialisierungsaufruf machen.

Ein explizites Handle wird als Parameter des Serialisierungsprozedurprototyps in der **\[ \_ \]** IDL-Datei angegeben, oder es kann auch mithilfe des expliziten Handleattributs im ACF angegeben werden. Der explizite Handleparameter wird verwendet, um den richtigen Serialisierungskontext für die Prozedur zu erstellen. Um den richtigen Kontext bei der Typserialisierung zu erstellen, generiert der Compiler die unterstützenden Routinen, die den expliziten [**\_ t-Handleparameter**](/windows/desktop/Midl/handle-t) als Serialisierungshand handle verwenden. Sie müssen ein gültiges Serialisierungshand handle beim Aufrufen einer Serialisierungsprozedur oder einer Serialisierungstypunterstützungsroutine verwenden.

 

 