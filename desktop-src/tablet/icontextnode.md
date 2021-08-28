---
description: Stellt einen Knoten in einer Struktur von -Objekten dar, die im Rahmen der Ink-Analyse erstellt werden.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: IContextNode-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9e6ca9e65b7c14f1df3af00acece8e2ba37c85d6a2193989ab232839f1863c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713464"
---
# <a name="icontextnode-interface"></a>IContextNode-Schnittstelle

Stellt einen Knoten in einer Struktur von -Objekten dar, die im Rahmen der Ink-Analyse erstellt werden.

## <a name="members"></a>Member

Die **IContextNode-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextNode** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IContextNode-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                  | Beschreibung                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddContextLink**](icontextnode-addcontextlink.md)                                   | Fügt der Kontextlinksammlung des **IContextNode-Objekts** einen neuen [**IContextLink**](icontextlink.md) hinzu.<br/>                                                                                                          |
| [**Addpropertydata**](icontextnode-addpropertydata.md)                                 | Fügt anwendungsspezifische Daten hinzu.<br/>                                                                                                                                                                         |
| [**Confirm**](icontextnode-confirm.md)                                                 | Ändert den Bestätigungstyp, der steuert, was das [**IInkAnalyzer-Objekt**](iinkanalyzer.md) über den **IContextNode ändern kann.**<br/>                                                                         |
| [**Containspropertydata**](icontextnode-containspropertydata.md)                       | Bestimmt, ob das **IContextNode-Objekt** Unter dem angegebenen Bezeichner gespeicherte Daten enthält.<br/>                                                                                                                |
| [**CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md) | Erstellt ein untergeordnetes **IContextNode-Objekt,** das nur Informationen zu Typ, Bezeichner und Speicherort enthält.<br/>                                                                                                          |
| [**CreateSubNode**](icontextnode-createsubnode.md)                                     | Erstellt ein neues untergeordnetes **IContextNode-Objekt.**<br/>                                                                                                                                                                       |
| [**DeleteContextLink**](icontextnode-deletecontextlink.md)                             | Löscht ein [**IContextLink-Objekt**](icontextlink.md) aus der Linksammlung des **IContextNode-Objekts.**<br/>                                                                                                         |
| [**DeleteSubNode**](icontextnode-deletesubnode.md)                                     | Entfernt einen untergeordneten **IContextNode.**<br/>                                                                                                                                                                                  |
| [**GetContextLinks**](icontextnode-getcontextlinks.md)                                 | Ruft eine Auflistung von [**IContextLink-Objekten**](icontextlink.md) ab, die Beziehungen mit anderen **IContextNode-Objekten** darstellt.<br/>                                                                          |
| [**Getid**](icontextnode-getid.md)                                                     | Ruft den Bezeichner für das **IContextNode-Objekt** ab.<br/>                                                                                                                                                          |
| [**Getlocation**](icontextnode-getlocation.md)                                         | Ruft die Position und Größe des **IContextNode-Objekts** ab.<br/>                                                                                                                                                    |
| [**GetParentNode**](icontextnode-getparentnode.md)                                     | Ruft den übergeordneten Knoten dieses **IContextNode** in der Kontextknotenstruktur ab.<br/>                                                                                                                                       |
| [**GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)                     | Ruft den Wert ab, der angibt, ob ein **IContextNode-Objekt** teilweise oder vollständig aufgefüllt ist.<br/>                                                                                                   |
| [**Getpropertydata**](icontextnode-getpropertydata.md)                                 | Ruft anwendungsspezifische Daten oder andere Eigenschaftsdaten unter Verwendung des angegebenen Bezeichners ab.<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | Ruft die Bezeichner ab, für die Eigenschaftsdaten enthalten sind.<br/>                                                                                                                                                        |
| [**GetStrokeCount**](icontextnode-getstrokecount.md)                                   | Ruft die Anzahl der Striche ab, die dem **IContextNode-Objekt zugeordnet** sind.<br/>                                                                                                                                       |
| [**GetStrokeId**](icontextnode-getstrokeid.md)                                         | Ruft den Strichbezeichner für den Strich ab, auf den durch einen Indexwert im **IContextNode-Objekt verwiesen** wird.<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | Ruft ein Array von Bezeichnern für die Striche im **IContextNode-Objekt** ab.<br/>                                                                                                                              |
| [**GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)                 | Ruft ein Array ab, das die Paketeigenschaftsdaten für den angegebenen Strich enthält.<br/>                                                                                                                                   |
| [**GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)   | Ruft ein Array ab, das die Paketeigenschaftsbezeichner für den angegebenen Strich enthält.<br/>                                                                                                                            |
| [**GetSubNodes**](icontextnode-getsubnodes.md)                                         | Ruft die direkten untergeordneten Knoten des **IContextNode-Objekts** ab.<br/>                                                                                                                                                   |
| [**Gettype**](icontextnode-gettype.md)                                                 | Ruft den Typ des **IContextNode-Objekts** ab.<br/>                                                                                                                                                                 |
| [**GetTypeName**](icontextnode-gettypename.md)                                         | Ruft einen für Menschen lesbaren Typnamen dieses **IContextNode ab.**<br/>                                                                                                                                                     |
| [**IsConfirmed**](icontextnode-isconfirmed.md)                                         | Ruft einen Wert ab, der angibt, ob **das IContextNode-Objekt** bestätigt wird. [**IInkAnalyzer kann**](iinkanalyzer.md) den Knotentyp und die zugeordneten Striche für bestätigten **IContextNode-Objekte nicht** ändern.<br/> |
| [**LoadPropertiesData**](icontextnode-loadpropertiesdata.md)                           | Erstellt die anwendungsspezifischen und internen Eigenschaftsdaten für ein Bytearray neu, das zuvor mit [**IContextNode::SavePropertiesData erstellt wurde.**](icontextnode-savepropertiesdata.md)<br/>                  |
| [**MoveSubNodeToPosition**](icontextnode-movesubnodetoposition.md)                     | Ordnet ein angegebenes untergeordnetes **IContextNode-Objekt** dem angegebenen Index neu an.<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | Entfernt anwendungsspezifische Daten.<br/>                                                                                                                                                                      |
| [**Wiedervererbung**](icontextnode-reparent.md)                                               | Verschiebt **dieses IContextNode-Objekt** aus der Subknotensammlung des übergeordneten Kontextknotens in die Auflistung der untergeordneten Knoten des angegebenen Kontextknotens.<br/>                                                                         |
| [**ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)               | Verschiebt Strichdaten von **diesem IContextNode** in den **angegebenen IContextNode.**<br/>                                                                                                                                    |
| [**SavePropertiesData**](icontextnode-savepropertiesdata.md)                           | Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaftsdaten für diesen **IContextNode enthält.**<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | Aktualisiert die Position und Größe dieses **IContextNode.**<br/>                                                                                                                                                            |
| [**SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)                     | Ändert den Wert, der angibt, ob **dieser IContextNode** teilweise oder vollständig aufgefüllt ist.<br/>                                                                                                                   |
| [**SetStrokes**](icontextnode-setstrokes.md)                                           | Ordnet diesem **IContextNode die angegebenen Striche zu.**<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Hinweise

Die Knotentypen werden in den Konstanten [Kontextknotentypen](context-node-types.md) beschrieben.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Methode, die einen **IContextNode untersucht.** Die -Methode führt Folgendes aus:

-   Ruft den Typ des Kontextknotens ab. Wenn der Kontextknoten ein nicht klassifizierter Ink-, Analysehinweis- oder benutzerdefinierter Recognizer-Knoten ist, ruft er eine Hilfsmethode auf, um bestimmte Eigenschaften des Knotentyps zu untersuchen.
-   Wenn der Knoten Unterknoten enthält, untersucht er jeden Unterknoten, indem er sich selbst aufruft.
-   Wenn der Knoten ein Ink-Blattknoten ist, werden die Strichdaten für den Knoten durch Aufrufen einer Hilfsmethode untersucht.

Mit der Ihe InkAnalysis-API können Sie einen Zeilenknoten erstellen, der Ink-Wörter und Textwörter enthält. Der Parser ignoriert diese gemischten Knoten jedoch und behandelt sie wie Fremdknoten. Dies wirkt sich auf die Analysegenauigkeit der Erkennung von Ink-Anmerkungen aus, wenn der Endbenutzer auf diesen gemischten Knoten schreibt oder um ihn herum schreibt.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Kontextknotentypen](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

