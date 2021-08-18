---
title: Anzeigen modaler Benutzeroberflächen
description: Anzeigen modaler Benutzeroberflächen
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player Plug-Ins, Anzeigen von Dialogfeldern und Meldungsfeldern
- Plug-Ins, Anzeigen von Dialogfeldern und Meldungsfeldern
- Benutzeroberflächen-Plug-Ins, Anzeigen von Dialogfeldern und Meldungsfeldern
- Ui-Plug-Ins, Anzeigen von Dialogfeldern und Meldungsfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addacfe2a309808f949c59a8ec11498417cb05a17cd6ab160ca1c08d2017a0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997240"
---
# <a name="displaying-modal-user-interfaces"></a>Anzeigen modaler Benutzeroberflächen

Benutzeroberflächen-Plug-Ins sollten keine modalen Dialogfelder oder Meldungsfelder als Reaktion auf Methodenaufrufe von Windows Media Player anzeigen. Zeigen Sie beispielsweise kein Meldungsfeld aus Ihrer Implementierung von **IWMPPluginUI::Create** an.

Wenn Sie ein Dialogfeld oder ein Meldungsfeld aus einer Implementierung einer Ui-Plug-In-Methode anzeigen müssen, die vom Player aufgerufen wird, müssen Sie die folgenden Schritte ausführen:

1.  Registrieren Sie eine neue Fenstermeldung mithilfe von **RegisterWindowMessage**.
2.  Senden Sie die Fenstermeldung, die Sie bei Ihrem Benutzeroberflächen-Plug-In-Fenster registriert haben, mit **postMessage**.
3.  Zeigt das Dialogfeld oder Meldungsfeld aus dem Meldungshandler für die neue Fenstermeldung an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**UI Plug-in Overview**](ui-plug-in-overview.md)
</dt> </dl>

 

 




