---
title: Serialisierungshandles
description: Eine Anwendung verwendet die serialisierenden Prozeduren oder die serialisierenden Unterstützungsroutinen, die vom MIDL-Compiler in Verbindung mit einem Satz von Bibliotheksfunktionen generiert werden, um ein Serialisierungshandle zu bearbeiten.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12995144e44fa6b4b91f021d544b53c03d732df22d46489ccc2cefe8d34c0fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925474"
---
# <a name="serialization-handles"></a>Serialisierungshandles

Eine Anwendung verwendet die serialisierenden Prozeduren oder die serialisierenden Unterstützungsroutinen, die vom MIDL-Compiler in Verbindung mit einem Satz von Bibliotheksfunktionen generiert werden, um ein Serialisierungshandle zu bearbeiten. Zusammen bieten diese Funktionen einen Mechanismus zum Anpassen der Art und Weise, wie eine Anwendung Daten serialisiert.

Ein Serialisierungshandles ist für jeden Serialisierungsvorgang erforderlich, und alle Serialisierungshandles müssen explizit von Ihnen verwaltet werden. Hierzu erstellen Sie zunächst ein gültiges Handle, indem Sie eine der folgenden Routinen aufrufen:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Sie geben das Handle mit einem Aufruf von [**MesHandleFree frei.**](/windows/desktop/api/Midles/nf-midles-meshandlefree) Nachdem das Handle erstellt oder erneut initialisiert wurde, stellt es einen gültigen Serialisierungskontext dar und kann je nach Typ des Handles zum Codieren oder Decodieren verwendet werden.

In diesem Abschnitt werden Serialisierungshandles und deren Verwendung in den folgenden Themen beschrieben:

-   [Implizite und explizite Handles im Vergleich](implicit-versus-explicit-handles.md)
-   [Serialisierungsstile](serialization-styles.md)
-   [Abrufen einer Codierungsidentität](obtaining-an-encoding-identity.md)

 

 




