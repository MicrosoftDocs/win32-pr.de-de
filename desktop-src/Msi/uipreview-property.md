---
description: Die Property-Eigenschaft des UIPreview-Objekts ist eine Lese-/Schreibeigenschaft, die den Zeichenfolgenwert einer benannten Installer-Eigenschaft darstellt, oder, wenn ihr ein Prozentzeichen (%) vorangestellt ist, der Wert einer Systemumgebungsvariablen für den aktuellen Prozess.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: UIPreview.Property-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 51ef7b4589372006241beff1e9c35180b32c4d358e817b8d380353c324ffd9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623203"
---
# <a name="uipreviewproperty-property"></a>UIPreview.Property-Eigenschaft

Die **Property-Eigenschaft** des [**UIPreview-Objekts**](uipreview-object.md) ist eine Lese-/Schreibeigenschaft, die den Zeichenfolgenwert einer benannten Installer-Eigenschaft darstellt, oder, wenn ihr ein Prozentzeichen (%) vorangestellt ist, der Wert einer Systemumgebungsvariablen für den aktuellen Prozess. Dies wird verfügbar gemacht, um eine ordnungsgemäße Anzeige von Dialogfeldern zu ermöglichen, die von Eigenschaftswerten abhängig sind. Es können Zeichenfolgen- oder ganzzahlige Werte angegeben werden. Eine nicht vorhandene Eigenschaft oder Umgebungsvariable entspricht dem Wert NULL.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Name einer Eigenschaft, bei dem die Groß-/Kleinschreibung beachtet wird, oder ein Name einer Umgebungsvariablen, der ein Prozentzeichen (%) vorangestellt ist, ohne Unterscheidung nach Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview ist als 000C109A-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                           |



 

 




