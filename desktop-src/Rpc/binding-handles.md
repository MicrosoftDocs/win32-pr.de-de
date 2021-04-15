---
title: Bindungs Handles
description: Bei der Bindung wird eine logische Verbindung zwischen einem Client Programm und einem Serverprogramm erstellt. Die Informationen, die die Bindung zwischen Client und Server verfasst haben, werden durch eine Struktur dargestellt, die als Bindungs Handle bezeichnet wird.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516847"
---
# <a name="binding-handles"></a>Bindungs Handles

Bei der Bindung wird eine logische Verbindung zwischen einem Client Programm und einem Serverprogramm erstellt. Die Informationen, die die Bindung zwischen Client und Server verfasst haben, werden durch eine Struktur dargestellt, die als Bindungs Handle bezeichnet wird.

Ein Bindungs Handle entspricht einem Datei Handle, das von der fopen-C-Lauf Zeit Bibliotheksfunktion zurückgegeben wird, oder einem Fenster Handle, das von der Funktion " [**kreatewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " zurückgegeben wird.

Wie bei diesen Handles kann Ihre Anwendung nicht direkt auf die Informationen im Bindungs handle zugreifen und diese bearbeiten. Die Informationen in einer Bindungs handle-Datenstruktur sind nur für die RPC-Laufzeitbibliotheken verfügbar. Sie stellen das Handle bereit. die Laufzeitbibliotheken greifen auf die entsprechenden Daten zu und bearbeiten Sie.

In diesem Abschnitt werden die Bindungs Handles in den folgenden Themen erläutert:

-   [Typen von Bindungs Handles](types-of-binding-handles.md)
-   [Client seitige Bindung](client-side-binding.md)
-   [Server seitige Bindung](server-side-binding.md)
-   [Vollständige und teilweise gebundene Handles](fully-and-partially-bound-handles.md)
-   [Interpretieren von Bindungs Informationen](interpreting-binding-information.md)
-   [Microsoft RPC-Binding-Handle Erweiterungen](microsoft-rpc-binding-handle-extensions.md)
-   [Bindungs handle-Funktionen](binding-handle-functions.md)
-   [Datenbank des RPC-namens Dienstanbieter](the-rpc-name-service-database.md)

 

 