---
description: Verwenden von Shellerweiterungen zum Implementieren eines kopierhook-Handlers.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Erstellen von Kopier-Hook-Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215945"
---
# <a name="how-to-create-copy-hook-handlers"></a>Erstellen von Kopier-Hook-Handlern

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für das Kopieren von Hook-Handlern spezifisch sind.

-   [Implementieren von Kopier-Hook-Handlern](#step-1-implementing-copy-hook-handlers)
-   [Registrieren von Kopier-Hook-Handlern](#step-2-registering-copy-hook-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-copy-hook-handlers"></a>Schritt 1: Implementieren von Kopier-Hook-Handlern

Wie bei allen Shellerweiterungs Handlern sind kopierhandler für den Kopiervorgang in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden. Sie exportieren zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**icopyhook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))eine Schnittstelle. Die Shell initialisiert den Handler direkt, sodass keine Initialisierungs Schnittstelle wie [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)erforderlich ist.

Die [**icopyhook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) -Schnittstelle verfügt über eine einzelne Methode, [**icopyhook:: copycallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)). Wenn ein Ordner gerade verschoben wird, ruft die Shell diese Methode auf. Sie übergibt eine Vielzahl von Informationen, einschließlich:

-   Der Name des Ordners.
-   Der Ziel-oder neue Name des Ordners.
-   Der Vorgang, der versucht wird.
-   Die Attribute der Quell-und Zielordner.
-   Ein Fenster Handle, das verwendet werden kann, um eine Benutzeroberfläche anzuzeigen.

Wenn die [**icopyhook:: copycallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) -Methode Ihres Handlers aufgerufen wird, gibt Sie einen der drei folgenden Werte zurück, um der Shell anzuzeigen, wie Sie fortfahren soll.



| Wert    | BESCHREIBUNG                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | Ermöglicht den Vorgang.                                                                                                                            |
| IDNO     | Verhindert den Vorgang in diesem Ordner. Die Shell kann mit allen anderen Vorgängen, die genehmigt wurden, fortgesetzt werden, z. b. einem Batch Kopiervorgang. |
| IDCANCEL | Verhindert den aktuellen Vorgang und bricht alle ausstehenden Vorgänge ab.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Schritt 2: Registrieren von Kopier-Hook-Handlern

Kopieren Sie Hook-Handler für Ordner unter dem Stammverzeichnis der **HKEY- \_ Klassen \_** Stamm \\ **Verzeichnis** \\ **shellex** \\ **copyhookhandlers** . Erstellen Sie einen Unterschlüssel von **copyhuokhandlers** , der für den Handler benannt ist, und legen Sie den Standardwert des unter Schlüssels auf das Zeichen folgen Format der Klassen Bezeichner-GUID (CLSID) des Handlers fest.

Das folgende Beispiel fügt den Unterschlüssel **mycopyhandler** der Liste der Kopier-Hook-Handler der Shell hinzu.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

Das Kopieren von Hook-Handlern für Drucker Objekte wird im Wesentlichen auf die gleiche Weise registriert. Der einzige Unterschied besteht darin, dass Sie Sie unter dem Unterschlüssel **HKEY \_ Classes \_ root** \\ **Printer** unter Key registrieren müssen.

## <a name="remarks"></a>Bemerkungen

Normalerweise können Benutzer und Anwendungen Ordner mit wenigen Einschränkungen kopieren, verschieben, löschen oder umbenennen. Durch Implementieren eines kopierhook-Handlers können Sie steuern, ob diese Vorgänge stattfinden. Beispielsweise können Sie durch Implementieren eines solchen Handlers verhindern, dass wichtige Ordner umbenannt oder gelöscht werden. Das Kopieren von Hook-Handlern kann auch für Drucker Objekte implementiert werden.

Kopieren von Hook-Handlern ist Global. Alle registrierten Handler werden von der Shell jedes Mal aufgerufen, wenn eine Anwendung oder ein Benutzer versucht, einen Ordner oder ein Drucker Objekt zu kopieren, zu verschieben, zu löschen oder umzubenennen. Der Handler führt den Vorgang selbst nicht aus. Sie genehmigt oder überprüft Sie nur. Wenn alle Handler eine Genehmigung durchführt, führt die Shell den Vorgang aus. Wenn ein Handler den Vorgang überprüft, wird er abgebrochen, und die restlichen Handler werden nicht aufgerufen. Kopieren von Hook-Handlern wird nicht über den Erfolg oder Misserfolg des Vorgangs informiert, sodass Sie nicht zum Überwachen von Datei Vorgängen verwendet werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Shellerweiterungshandlern](handlers.md)
</dt> <dt>

[**Icopyhook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
