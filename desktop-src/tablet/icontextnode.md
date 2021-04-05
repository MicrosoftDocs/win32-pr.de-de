---
description: Stellt einen Knoten in einer Struktur von Objekten dar, die als Teil der frei Hand Analyse erstellt werden.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Icontextnode-Schnittstelle (iacom. h)
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
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041763"
---
# <a name="icontextnode-interface"></a>Icontextnode-Schnittstelle

Stellt einen Knoten in einer Struktur von Objekten dar, die als Teil der frei Hand Analyse erstellt werden.

## <a name="members"></a>Member

Die **icontextnode** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Icontextnode** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **icontextnode** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addcontextlink**](icontextnode-addcontextlink.md)                                   | Fügt der Kontext Link Auflistung des **icontextnode** -Objekts einen neuen [**icontextlink**](icontextlink.md) hinzu.<br/>                                                                                                          |
| [**AddPropertyData**](icontextnode-addpropertydata.md)                                 | Fügt eine bestimmte anwendungsspezifische Daten hinzu.<br/>                                                                                                                                                                         |
| [**Confirm**](icontextnode-confirm.md)                                                 | Ändert den bestäalisierungstyp, der steuert, was das [**iinkanalyzer**](iinkanalyzer.md) -Objekt über den **icontextnode** ändern kann.<br/>                                                                         |
| [**ContainsPropertyData**](icontextnode-containspropertydata.md)                       | Bestimmt, ob das **icontextnode** -Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind.<br/>                                                                                                                |
| [**"Kreatepartiallypopulatedsubnode"**](icontextnode-createpartiallypopulatedsubnode.md) | Erstellt ein untergeordnetes **icontextnode** -Objekt, das nur Informationen zu Typ, Bezeichner und Speicherort enthält.<br/>                                                                                                          |
| [**"Kreatesubnode"**](icontextnode-createsubnode.md)                                     | Erstellt ein neues untergeordnetes **icontextnode** -Objekt.<br/>                                                                                                                                                                       |
| [**Deletecontextlink**](icontextnode-deletecontextlink.md)                             | Löscht ein [**icontextlink**](icontextlink.md) -Objekt aus der Link Auflistung des **icontextnode** -Objekts.<br/>                                                                                                         |
| [**Delta esubnode**](icontextnode-deletesubnode.md)                                     | Entfernt einen untergeordneten **icontextnode**.<br/>                                                                                                                                                                                  |
| [**Getcontextlinks**](icontextnode-getcontextlinks.md)                                 | Ruft eine Auflistung von [**icontextlink**](icontextlink.md) -Objekten ab, die Beziehungen mit anderen **icontextnode** -Objekten darstellt.<br/>                                                                          |
| [**GetId**](icontextnode-getid.md)                                                     | Ruft den Bezeichner für das **icontextnode** -Objekt ab.<br/>                                                                                                                                                          |
| [**GetLocation**](icontextnode-getlocation.md)                                         | Ruft die Position und die Größe des **icontextnode** -Objekts ab.<br/>                                                                                                                                                    |
| [**Getparameentnode**](icontextnode-getparentnode.md)                                     | Ruft den übergeordneten Knoten dieses **icontextnode** in der Kontext Knoten Struktur ab.<br/>                                                                                                                                       |
| [**Getpartiallyausgefüllt**](icontextnode-getpartiallypopulated.md)                     | Ruft den Wert ab, der angibt, ob ein **icontextnode** -Objekt teilweise aufgefüllt oder vollständig ausgefüllt ist.<br/>                                                                                                   |
| [**GetPropertyData**](icontextnode-getpropertydata.md)                                 | Ruft anwendungsspezifische Daten oder andere Eigenschafts Daten mit dem angegebenen Bezeichner ab.<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | Ruft die Bezeichner ab, für die Eigenschafts Daten vorhanden sind.<br/>                                                                                                                                                        |
| [**Getstrokecount**](icontextnode-getstrokecount.md)                                   | Ruft die Anzahl der Striche ab, die dem **icontextnode** -Objekt zugeordnet sind.<br/>                                                                                                                                       |
| [**Getstrokeid**](icontextnode-getstrokeid.md)                                         | Ruft den Strich Bezeichner für den Strich ab, auf den durch einen Indexwert im **icontextnode** -Objekt verwiesen wird.<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | Ruft ein Array von bezeichern für die Striche innerhalb des **icontextnode** -Objekts ab.<br/>                                                                                                                              |
| [**Getstrokepacketdatabyid**](icontextnode-getstrokepacketdatabyid.md)                 | Ruft ein Array ab, das die Paket Eigenschafts Daten für den angegebenen Strich enthält.<br/>                                                                                                                                   |
| [**Getstrokepacketdescriptionbyid**](icontextnode-getstrokepacketdescriptionbyid.md)   | Ruft ein Array ab, das die Paket Eigenschaften Bezeichner für den angegebenen Strich enthält.<br/>                                                                                                                            |
| [**Getsubnodes**](icontextnode-getsubnodes.md)                                         | Ruft die direkt untergeordneten Knoten des **icontextnode** -Objekts ab.<br/>                                                                                                                                                   |
| [**GetType**](icontextnode-gettype.md)                                                 | Ruft den Typ des **icontextnode** -Objekts ab.<br/>                                                                                                                                                                 |
| [**Gettyname**](icontextnode-gettypename.md)                                         | Ruft einen lesbaren Typnamen dieses **icontextnode** ab.<br/>                                                                                                                                                     |
| [**Isbestätigt**](icontextnode-isconfirmed.md)                                         | Ruft einen Wert ab, der angibt, ob das **icontextnode** -Objekt bestätigt ist. Der Knotentyp und die zugehörigen Striche für bestätigte **icontextnode** -Objekte können von [**iinkanalyzer**](iinkanalyzer.md) nicht geändert werden.<br/> |
| [**Loadpropertiesdata**](icontextnode-loadpropertiesdata.md)                           | Erstellt die anwendungsspezifischen und internen Eigenschaften Daten für ein Bytearray, das zuvor mit [**icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)erstellt wurde.<br/>                  |
| [**"Muvesbnodebug"**](icontextnode-movesubnodetoposition.md)                     | Ordnet ein angegebenes untergeordnetes **icontextnode** -Objekt an den angegebenen Index zurück.<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | Entfernt anwendungsspezifische Daten.<br/>                                                                                                                                                                      |
| [**Neu zuordnen**](icontextnode-reparent.md)                                               | Verschiebt dieses **icontextnode** -Objekt aus der Auflistung der untergeordneten Knoten des übergeordneten Kontext Knotens in die Auflistung der untergeordneten Knoten des angegebenen Kontext Knotens.<br/>                                                                         |
| [**Analyse von "Analyse"**](icontextnode-reparentstrokebyidtonode.md)               | Verschiebt die Strich Daten aus diesem **icontextnode** in den angegebenen **icontextnode**.<br/>                                                                                                                                    |
| [**Savepropertiesdata**](icontextnode-savepropertiesdata.md)                           | Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaften Daten für diesen **icontextnode** enthält.<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | Aktualisiert die Position und Größe dieses **icontextnode**.<br/>                                                                                                                                                            |
| [**Setpartiallyausgefüllt**](icontextnode-setpartiallypopulated.md)                     | Ändert den Wert, der angibt, ob dieser **icontextnode** teilweise oder vollständig ausgefüllt ist.<br/>                                                                                                                   |
| [**Setstrokes**](icontextnode-setstrokes.md)                                           | Ordnet diesem **icontextnode** die angegebenen Striche zu.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Die Knoten Typen werden in den [Kontext Knoten Typen](context-node-types.md) -Konstanten beschrieben.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Methode, die einen **icontextnode** untersucht. die-Methode führt Folgendes aus:

-   Ruft den Typ des Kontext Knotens ab. Handelt es sich bei dem Kontext Knoten um einen nicht klassifizierten Ink-, Analyse-oder benutzerdefinierten Erkennungs Knoten, wird eine Hilfsmethode aufgerufen, um bestimmte Eigenschaften des Knoten Typs zu untersuchen.
-   Wenn der Knoten über untergeordnete Knoten verfügt, werden die einzelnen unter Knoten durch Aufrufen von sich selbst untersucht.
-   Wenn der Knoten ein frei Hand Blattknoten ist, werden die Strich Daten für den Knoten durch Aufrufen einer Hilfsmethode untersucht.

Die IHE InkAnalysis-API ermöglicht es Ihnen, einen Zeilen Knoten zu erstellen, der frei Hand Wörter und Text Wörter enthält. Der Parser ignoriert diese gemischten Knoten jedoch und behandelt Sie wie fremde Knoten. Dies hat Auswirkungen auf die Verarbeitungsgenauigkeit bei der Erkennung von frei Hand Anmerkungen, wenn der Endbenutzer diesen gemischten Knoten ein-oder eingibt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnodes**](icontextnodes.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

