---
title: ObjectModel-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IObjectModelProvider, einschließlich Informationen zu Methoden. Das ObjectModel-Steuerelementmuster wird verwendet, um einen Zeiger auf das zugrunde liegende Objektmodell eines Dokuments verfügbar zu machen.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des ObjectModel-Steuerelementmusters
- Benutzeroberflächenautomatisierung,ObjectModel-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IObjectModelProvider
- IObjectModelProvider
- Implementieren Benutzeroberflächenautomatisierung ObjectModel-Steuerelementmusters
- ObjectModel-Steuerelementmuster
- Steuerelementmuster,IObjectModelProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung ObjectModel
- Steuerelementmuster,ObjectModel
- interfaces,IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62081f8fb841e7827f589fd2441c7b6411810f9a71c1c1962a0dfcf8b0e37180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114993"
---
# <a name="objectmodel-control-pattern"></a>ObjectModel-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IObjectModelProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)einschließlich Informationen zu Methoden. Das **ObjectModel-Steuerelementmuster** wird verwendet, um einen Zeiger auf das zugrunde liegende Objektmodell eines Dokuments verfügbar zu machen.

Viele Anwendungen implementieren Rich-Object-Modelle, die einen Mehrwert über das hinaus bieten, was Microsoft Benutzeroberflächenautomatisierung bietet. Mit diesem Steuerelementmuster kann ein Client von einem Benutzeroberflächenautomatisierung Element in das zugrunde liegende Objektmodell navigieren.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ObjectModel-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Die [**IObjectModelProvider::GetUnderlyingObjectModel-Methode**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) sollte einen Zeiger auf das Objekt zurückgeben, das dem Element der Quellbenutzeroberfläche so nahe wie möglich ist. In einem Webbrowser sollte beispielsweise ein Benutzeroberflächenautomatisierung Anbieter für ein einzelnes Element einen Objektmodellzeiger für das Element zurückgeben. Das Zurückgeben eines Objektmodellzeigers für das Dokumentstammverzeichnis wäre weitaus weniger nützlich.
-   Es wird  erwartet, dass der Client des ObjectModel-Steuerelementmusters über die IID für die gesuchte Schnittstelle verfügt. Daher reicht es aus, einen einfachen [**IUnknown-Zeiger**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) zurückzugeben.
-   Da Benutzeroberflächenautomatisierung den Zeiger auf den Clientprozess marshallt, sollte der Anbieter erwarten, dass der Client mithilfe von COM-Methoden (Standard Component Object Model) auf das Objektmodell zugreift.

## <a name="required-members-for-iobjectmodelprovider"></a>Erforderliche Member für **IObjectModelProvider**

Die folgende Methode ist für die Implementierung der [**IObjectModelProvider-Schnittstelle**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) erforderlich.



| Erforderliche Member                                                                             | Memberart | Hinweise                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Methode      | Gibt einen COM-Zeiger auf das zugrunde liegende Objektmodell zurück. Es wird erwartet, dass der Client die [**IUnknown::QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufruft, um bestimmte Objektmodellzeiger abzurufen. |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 