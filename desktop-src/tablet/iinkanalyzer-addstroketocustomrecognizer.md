---
description: Fügt einem benutzerdefinierten Recognizer-Knoten Strichdaten für einen einzelnen Strich hinzu.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: IInkAnalyzer::AddStrokeToCustomRecognizer-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0a3ce58f462053b48e6cecdc7eb276a1e162f88b0e7de373648a537b3b712cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967329"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>IInkAnalyzer::AddStrokeToCustomRecognizer-Methode

Fügt einem benutzerdefinierten Recognizer-Knoten Strichdaten für einen einzelnen Strich hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulStrokeId* \[ In\]
</dt> <dd>

Der Bezeichner für den hinzuzufügenden Strich.

</dd> <dt>

*ulStrokePacketDataCount* \[ In\]
</dt> <dd>

Die Anzahl der Pakete im Strich.

</dd> <dt>

*plStrokePacketData* \[ In\]
</dt> <dd>

Ein Array, das die Paketdaten für den Strich enthält.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ In\]
</dt> <dd>

Die Anzahl der Paketeigenschaften in jedem Paket.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ In\]
</dt> <dd>

Ein Array, das die Paketeigenschaftsbezeichner enthält.

</dd> <dt>

*pCustomRecognizer* \[ In\]
</dt> <dd>

Der [**IContextNode vom**](icontextnode.md) Typ **CustomRecognizer,** dem der Strich hinzugefügt werden soll.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

Der [**IContextNode,**](icontextnode.md) dem das Ink Analyzer den Strich hinzugefügt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodeStrokeAddedTo* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn *ppContextNodeStrokeAddedTo* **NULL ist,** gibt dies an, dass der Aufrufer nicht am Rückgabewert der Methode interessiert ist.

[**IInkAnalyzer fügt**](iinkanalyzer.md) den Strich einem [**IContextNode**](icontextnode.md) vom Typ **CustomRecognizer** hinzu (siehe [Kontextknotentypen](context-node-types.md)). Dieser Knoten befindet sich in der Unterknotensammlung des Stammknotens (siehe [**IInkAnalyzer::GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**IContextNode::GetSubNodes-Methoden).**](icontextnode-getsubnodes.md)

Der [**IInkAnalyzer**](iinkanalyzer.md) weist dem Strich den Kulturbezeichner des aktiven Eingabethreads zu und fügt den Strich dem ersten **UnclassifiedInk-Knoten** unter dem **CustomRecognizer-Knoten** hinzu. Wenn kein **Knoten UnclassifiedInk vorhanden** ist, wird er erstellt. Wenn der dem **CustomRecognizer-Knoten** zugeordnete [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) den Kulturbezeichner nicht unterstützt, setzt **der IInkAnalyzer** die Analyse fort und generiert eine [**IAnalysisWarning-Warnung.**](ianalysiswarning.md) Diese Warnung hat den [**AnalysisWarningCode-Wert**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ LanguageIdNotRespected.**

*plStrokePacketData enthält* Paketdaten für alle Punkte im Strich. *pStrokePacketDescriptionGuids* enthält die GUIDs (Globally Unique Identifiers), die die Typen von Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind. Eine vollständige Liste der verfügbaren Paketeigenschaften finden Sie unter [PacketPropertyGuids-Konstanten.](packetpropertyguids-constants.md)

Diese Methode erweitert den verfeckten Bereich auf die Vereinigung des aktuellen Werts des Region und des Begrenzungsfelds des hinzugefügten Strichs.

Der [**IInkAnalyzer gibt**](iinkanalyzer.md) unter den folgenden Umständen **ein HRESULT** von E **\_ INVALIDARG** zurück.

-   Der [**IInkAnalyzer enthält**](iinkanalyzer.md) bereits einen Strich mit demselben Bezeichner wie der Strich, der hinzugefügt werden soll.
-   Der *pCustomRecognizer-Parameter* enthält einen benutzerdefinierten Recognizer-Knoten, der einem anderen [**IInkAnalyzer-Objekt zugeordnet**](iinkanalyzer.md) ist.
-   Der *pCustomRecognizer-Parameter* enthält einen [**IContextNode,**](icontextnode.md) der nicht vom **Typ CustomRecognizer ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Kontextknotentypen](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesToCustomRecognizer-Methode**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

