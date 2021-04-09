---
title: Implementieren eines Client-Side (Proxy) Benutzeroberflächenautomatisierungs-Anbieters
description: In diesem Thema wird beschrieben, wie ein Proxy Anbieter für ein nicht unterstütztes Steuerelement geschrieben und der Liste der von Client Anwendungen verwendeten Proxys hinzugefügt wird.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Benutzeroberflächen Automatisierung, Client seitige Anbieter Implementierung
- UI-Automatisierung, Anbieter Implementierung
- Benutzeroberflächen Automatisierung, Implementieren von Client seitigen Anbietern
- Benutzeroberflächen Automatisierung, Implementieren von Anbietern
- UI-Automatisierung, Proxys
- proxies
- Client seitige Anbieter
- Anbieter, implementieren
- Implementieren von Client seitigen Anbietern
- Implementieren von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2bdb4a94ba6e693792508de5c573317299b0d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039078"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementieren eines Client-Side (Proxy) Benutzeroberflächenautomatisierungs-Anbieters

Die Microsoft-Benutzeroberflächen Automatisierung bietet eine Reihe von Proxys für die meisten Standard Steuerelemente, wie z. b. die in Microsoft Win32, Windows Forms und Windows Presentation Foundation (WPF) verwendeten Anwendungen. Viele benutzerdefinierte Steuerelemente und Steuerelemente von Drittanbietern implementieren jedoch keine nativen Benutzeroberflächenautomatisierungs-Anbieter. Um für Benutzeroberflächenautomatisierungs-Client Anwendungen zugänglich zu sein, müssen diese Steuerelemente mit Client seitigen Anbietern, auch als *Proxy Anbieter oder Proxys* bezeichnet, bereitgestellt werden. 

In diesem Thema wird beschrieben, wie ein Proxy Anbieter für ein nicht unterstütztes Steuerelement geschrieben und der Liste der von Client Anwendungen verwendeten Proxys hinzugefügt wird. Es umfasst die folgenden Themen:

-   [Was ist ein Proxy?](#what-is-a-proxy)
-   [Was ist eine proxyfactory?](#what-is-a-proxy-factory)
-   [Proxyfactory-Zuordnung](#proxy-factory-mapping)
-   [Standard Proxys verwalten](#managing-default-proxies)
-   [Zugehörige Themen](#related-topics)

Codebeispiele, die die Implementierung von Proxy Anbietern veranschaulichen, finden Sie unter Gewusst [-wie-Themen für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="what-is-a-proxy"></a>Was ist ein Proxy?

Bei einem Client seitigen Anbieter oder Proxy handelt es sich um ein Objekt, das die [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle für ein Steuerelement implementiert, das nicht über eine eigene **IRawElementProviderSimple** -Implementierung verfügt. Ohne einen Proxy ist ein solches Steuerelement für die Automatisierung der Benutzeroberfläche größtenteils nicht transparent, sodass nur grundlegende Informationen, die über das Fenster Handle (**HWND**) verfügbar sind, bereitgestellt werden können, z. b. die Steuerungs Position

## <a name="what-is-a-proxy-factory"></a>Was ist eine proxyfactory?

Jeder Proxy benötigt eine entsprechende *proxyfactory*, bei der es sich um ein Objekt handelt, das die [**iuiautomationproxyfactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) -Schnittstelle verfügbar macht. Die Benutzeroberflächen Automatisierung verwaltet eine interne Tabelle von *proxyfactory-Einträgen*, die jeweils einen Verweis auf die proxyfactory für jeden Proxy und einen Satz von Bedingungen enthalten. Wenn die Benutzeroberflächen Automatisierung auf ein Steuerelement stößt, das keine native [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Implementierung hat, sucht es nach einem proxyfactory-Eintrag, dessen Bedingungen darauf hindeuten, dass das Steuerelement unterstützt wird. Die Benutzeroberflächen Automatisierung durchsucht die Tabelle von Anfang an, und wenn ein entsprechender Eintrag gefunden wird, ruft die Benutzeroberflächen Automatisierung die [**iuiautomationproxyfactory:: kreateprovider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) -Methode der Factory auf. Wenn der übereinstimmende Proxy erfolgreich erstellt wurde, beendet die Benutzeroberflächen Automatisierung die Suche und verwendet das neu erstellte Proxy Objekt. Andernfalls setzt die Benutzeroberflächen Automatisierung die Suche fort.

Eine Client Anwendung erstellt mithilfe der [**iuiautomation:: deateproxyfactoryentry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) -Methode, die einen [**iuiautomationproxyfactoryentry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) -Schnittstellen Zeiger zurückgibt, eine Instanz eines proxyfactoryeintrags. Clients verwenden Methoden, die von **iuiautomationproxyfactoryentry** verfügbar gemacht werden, um den Satz von Bedingungen anzugeben, den die proxyfactory zum Erstellen des Proxys verwendet.

Beim Aufrufen von [**iuiautomationproxyfactory::-Anbieter**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider)übergibt die Benutzeroberflächen Automatisierung Parameter, die vom proxyfactory-Objekt verwendet werden können, um zu bestimmen, ob der Proxy das benutzerdefinierte Steuerelement angemessen unterstützt. Wenn dies der Fall ist, erstellt die proxyfactory eine Instanz des Proxys und gibt den [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstellen Zeiger zurück. Andernfalls wird ein **null** -Zeiger zurückgegeben.

## <a name="proxy-factory-mapping"></a>Proxyfactory-Zuordnung

Standardmäßig durchsucht die Benutzeroberflächen Automatisierung die proxyfactory-Tabelle in der folgenden Reihenfolge.



| Auftrag | Proxy                        | BESCHREIBUNG                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: nicht-Steuerungs Proxy | Für Windows mit dem genauen Klassennamen oder Basisklassen Namen "ComboBoxEx32".         |
| 2     | Microsoft: nicht-Steuerungs Proxy | Für Windows mit dem genauen Klassennamen oder Basisklassen Namen "workerw".              |
| 3     | Microsoft: nicht-Steuerungs Proxy | Für Windows mit dem genauen Klassennamen oder Basisklassen Namen "shelldll \_ defview".    |
| 4     | Microsoft: Container Proxy   | Für Windows mit dem genauen Klassennamen oder Basisklassen Namen " \# 32770".              |
| 5     | Microsoft: Container Proxy   | Für Windows mit einem Klassennamen oder Basisklassen Namen, der "afxcontrolbar" enthält.     |
| 6     | Microsoft: TreeView-Proxy    | Für Windows mit einem Klassennamen oder Basisklassen Namen, der "SysTreeView32" enthält.     |
| 7     | Microsoft: ListView-Proxy    | Für Windows mit einem Klassennamen oder Basisklassen Namen, der "SysListView32" (1) enthält. |
| 8     | Microsoft: ListView-Proxy    | Für Windows mit einem Klassennamen oder Basisklassen Namen, der "SysListView32" (2) enthält. |
| 9     | Microsoft: MSAA-Proxy        | Für ein beliebiges Fenster.                                                                  |



 

Proxys 7 und 8 sind doppelte Einträge für das SysListView32-Steuerelement. Ohne Änderung wird der Proxy 7 immer für das SysListView32-Steuerelement verwendet, und Proxy 8 wird nie verwendet. Proxy 8 wird nur für sichtbare Listenelemente verwendet und wird in der Regel von Client Anwendungen verwendet, die nur mit sichtbaren Elementen oder strengen Leistungsanforderungen funktionieren. Diese Clients können Proxy 7 entfernen.

Proxy 9, der Microsoft-Active Accessibility zum Benutzeroberflächenautomatisierungs-Proxy, sollte immer der letzte Eintrag in der Tabelle sein. Dadurch wird die Microsoft-Active Accessibility Fall Back Funktion für Steuerelemente aktiviert, die Microsoft Active Accessibility implementieren, aber nicht für die Benutzeroberflächen Automatisierung.

Wenn Sie Einträge in der proxyfactory-Tabelle ändern, sollten Sie die neue Position der Einträge sorgfältig auswerten. Es wird empfohlen, dass Einträge für benutzerdefinierte Proxys nach den nicht-Steuerelement-und Container Proxys platziert werden, aber vor dem Microsoft-Active Accessibility dem Benutzeroberflächenautomatisierungs Auch wenn es möglich ist, dass Code im-aufrufruf von "" erstellt wird [**, um zu bestimmen,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) ob ein bestimmtes Fenster Handle (**HWND**) unterstützt werden soll, ist es effizienter, die Benutzeroberflächen Automatisierung die Auswahl des Proxys basierend auf dem Klassennamen und den bedingten Code in der Methode " **kreateprovider** " minimal zu halten.

Die Benutzeroberflächen Automatisierung verwaltet für jeden Client eine separate proxyfactory-Tabelle. Wenn ein Client seine Proxy Tabelle ändert, wirken sich die Änderungen nur auf den Client selbst aus. andere Clients sind nicht betroffen.

## <a name="managing-default-proxies"></a>Standard Proxys verwalten

Wenn eine Client Anwendung das [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) -Objekt erstellt, enthält die proxyfactory-Tabelle anfänglich nur Einträge für die standardmäßigen Proxy Anbieter für Standard Steuerelemente. Mithilfe der [**iuiautomationproxyfactor ymapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) -Schnittstelle können Clients neue Einträge hinzufügen, unerwünschte Einträge entfernen, die Reihenfolge von Einträgen ändern usw. Ein Client kann einen **iuiautomationproxyfactorymapping** -Schnittstellen Zeiger abrufen, indem er die [**iuiautomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) -Methode aufruft.

Die Tabelle verfügbarer Proxys enthält eine [**iuiautomationproxyfactor yentry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) -Schnittstelle für jeden Proxy. Jeder **iuiautomationproxyfactoryentry** gibt die [**iuiautomationproxyfactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) und die Steuerelement Klasse an, die der Proxy bedient, und definiert, wie Ereignisse behandelt werden.

Die Tabelle der Proxys wird durch eine [**iuiautomationproxyfactor ymapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) -Schnittstelle dargestellt, die von der [**iuiautomation::P roxyfactor ymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) -Eigenschaft abgerufen werden kann. Eine Anwendung kann **iuiautomationproxyfactorymapping** -Methoden zum Hinzufügen und Löschen von Proxys verwenden. Um einen neuen Eintrag zu erstellen, der dieser Tabelle hinzugefügt werden soll, verwenden Sie [**iuiautomation:: deateproxyfactoryentry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) zum Abrufen der Schnittstelle, und verwenden Sie dann die [**iuiautomationproxyfactoryentry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) -Methoden, um die anwendbare Steuerelement Klasse und das Verhalten des Proxys zu definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Benutzeroberflächenautomatisierungs-Anbieters für Client-Side (Proxy)](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md)
</dt> </dl>

 

 