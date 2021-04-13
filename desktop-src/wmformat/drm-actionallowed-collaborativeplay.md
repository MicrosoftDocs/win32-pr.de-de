---
title: DRM_ActionAllowed_CollaborativePlay
description: Das DRM- \_ Aktions zugelassene \_ kollaborativeplay-Attribut gibt an, ob die Lizenz den Inhalt gemeinsam spielen kann.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389914"
---
# <a name="drm_actionallowed_collaborativeplay"></a>DRM- \_ Aktions zugelassene \_ kollaborativeplay

Das **DRM- \_ Aktions zugelassene \_ kollaborativeplay** -Attribut gibt an, ob die Lizenz den Inhalt gemeinsam spielen kann.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Aktions zulässige \_ kollaborative Zusammenspiel

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Die gemeinsame Wiedergabe Berechtigung gilt für die Wiedergabe geschützter Inhalte als Teil einer kollaborativen Sitzung mithilfe von Peer-to-Peer-Diensten. Beispielsweise können Benutzer von MSN Messenger 2004 geschützte Inhalte in einer MusicMix-Sitzung wiedergeben. Dieses Recht kann nur verwendet werden, um eine geschützte Datei gleichzeitig zu einer einzelnen Sitzung beizutragen, und alle Benutzer, die an der Sitzung teilnehmen, müssen online sein, damit der Inhalt wieder hergestellt werden kann.

Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




