---
description: Bei der Registrierung handelt es sich um eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows Anwendungen und Diensten, die auf dem Server ausgeführt Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struktur der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2eb63d49db37bc23eee56bb845c9c5dedf9df7ce4ce610ff8ade500e97cb88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763493"
---
# <a name="structure-of-the-registry"></a>Struktur der Registrierung

Bei der Registrierung handelt es sich um eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows Anwendungen und Diensten, die auf dem Server ausgeführt Windows. Die Daten sind in einem Strukturformat strukturiert. Jeder Knoten in der Struktur wird als Schlüssel *bezeichnet.* Jeder Schlüssel kann sowohl Unterschlüssel *als auch Dateneinträge* enthalten, die als Werte *bezeichnet werden.* Manchmal sind alle Daten, die eine Anwendung benötigt, das Vorhandensein eines Schlüssels. in anderen Zeiten öffnet eine Anwendung einen Schlüssel und verwendet die dem Schlüssel zugeordneten Werte. Ein Schlüssel kann eine beliebige Anzahl von Werten enthalten, und die Werte können in beliebiger Form sein. Weitere Informationen finden Sie unter [Registrierungswerttypen und](registry-value-types.md) [Größenbeschränkungen für Registrierungselemente.](registry-element-size-limits.md)

Jeder Schlüssel hat einen Namen, der aus mindestens einem druckbaren Zeichen besteht. Bei Schlüsselnamen wird die Schreibung nicht beachtet. Schlüsselnamen dürfen nicht den schrägen Schrägstrich () enthalten, es können jedoch \\ beliebige andere druckbare Zeichen verwendet werden. Wertnamen und Daten können den schrägen Schrägstrich enthalten.

Der Name jedes Unterschlüssels ist in Bezug auf den Schlüssel, der sich direkt darüber in der Hierarchie befindet, eindeutig. Schlüsselnamen werden nicht in andere Sprachen lokalisiert, obwohl Werte sein können.

Die folgende Abbildung zeigt eine Beispielstruktur für Registrierungsschlüssel, die vom Registrierungs-Editor angezeigt wird.

![Fenster "Registrierungs-Editor"](images/regtree.png)

Jede der Strukturen **unter** Arbeitsplatz ist ein Schlüssel. Der **HKEY \_ LOCAL \_ MACHINE-Schlüssel** verfügt über die folgenden Unterschlüssel: **HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** und **SYSTEM**. Jeder dieser Schlüssel verfügt wiederum über Unterschlüssel. Beispielsweise verfügt der **HARDWARE-Schlüssel** über die Unterschlüssel **DESCRIPTION,** **DEVICEMAP** und **RESOURCEMAP.** Der **DEVICEMAP-Schlüssel** verfügt über mehrere Unterschlüssel, einschließlich **VIDEO**.

Jeder Wert besteht aus einem Wertnamen und den zugehörigen Daten(sofern möglich). **MaxObjectNumber und** **VgaCompatible sind** Werte, die Daten unter dem **Unterschlüssel VIDEO** enthalten.

Eine Registrierungsstruktur kann 512 Ebenen tief sein. Sie können bis zu 32 Ebenen gleichzeitig über einen einzelnen Registrierungs-API-Aufruf erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
